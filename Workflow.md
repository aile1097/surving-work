## Workflow for build orthomosaic & 3D model in Agisoft Metashape



**Import photo file into project**
`Workflow` - `add folder`

**Check coordinates in `Setting`** (The requirement is to use the TWG97 coordinate system, but the UAV provides data in WGS84.)

**Align photo**
`Workflow` - `Align photos`

**Optimize figure**
`Optimize Cameras`


**Filter/Create tie point **
(**3 times, optimize after filtering each time**)
`Model` - `Gradual Selection` - `Reprojection Error` 
`Optimize`

`Model` - `Gradual Selection` - `Projection Uncertainly` 
`Optimize`

`Model` - `Gradual Selection` - `Image Count`
`Optimize`

**Import control point file `.csv` or `.txt` into project**
`Refrence`-`Import`

**Delete control points unnecessary** (**Operate in `Markers` window**)
Find the point you need - `Invert Selection` -`Delete Markers`

**Filter photos include control points**
`Filter Photos by Markers`

![image](https://hackmd.io/_uploads/SyVPVtQvA.png)

**Manual operation, align the control point (flag icon) in each photo filtered to the APT(航測標)**

**Optimize photo**
`Optimize Cameras`

**Build Dense Cloud**
`Workflow` - `Build Dense Cloud`

**Build Mesh**

`Workflow` - `Build Mesh`

**Build Orthomosaic**

`Workflow` - `Build Orthomosaic`



---------------
Refrence:
[Agisoft Metashape - Complete Tutorial (Cloud, Mesh, DSM, DTM, Classify, Orthoimage - No GCPs)](https://youtu.be/je79gV8HsZI)
