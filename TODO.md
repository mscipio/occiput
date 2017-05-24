======================================================
TODO list : Occiput - Tomographic Vision - version 1.1
======================================================

## <span style="color:blue">occiput TODO list:</span>

- <span style="color:blue">throw errors if loading proiections of a different shape/size of the target pet object</span>
- <span style="color:blue">add simulation function to Pet_Dynamic_Scan object (ability to ptoject a 4D dynamic phantom)</span>
- <span style="color:blue">add OSL algorithm for image reconstruction with smoothing or kinetic prior</span>
- <span style="color:blue">check for Transformation matrix input in *osem_reconstruction_4D*</span>
        if transformation is None:  
            transformation = RigidTransform((tx,ty,tz,0,0,0)) 
        else: 
            transformation = copy.copy(transformation)
            transformation.x = transformation.x + tx
            transformation.y = transformation.y + ty
            transformation.z = transformation.z + tz
- <span style="color:blue">BUG FIX: when compression is enabled, self.project_activity() should return a compressed projection even when there is no listmode involved. </span>
- <span style="color:blue">BUG FIX: PET_DynamicScan: osem_reconstruction() fails when sensitivity is not defined. </span>
- <span style="color:blue">BUG FIX: PET_DynamicScan: osem_reconstruction() output a reversed-z slice ordering when slicing from pet to pet2D rather than when visualizing a 4D reconstruction of the 3D volume</span>
- <span style="color:red">BUG FIX: PET_DynamicScan and PET_Multi2D_Scan produce reconstructed images of different scale (maybe because of how the prompts are summed up togheter when creating a PET_Multi2D_Scan from a 3D listmode) </span>
- <span style="color:blue">CHECK: PET_DynamicScan: osem_reconstruction() seems to produce different result (with same subset_size and iteration number) if applied to the entire volume or just to a single frame </span>



