---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PlayEnhMetaFile function


## -description


The <b>PlayEnhMetaFile</b> function displays the picture stored in the specified enhanced-format metafile.


## -parameters




### -param hdc [in]

A handle to the device context for the output device on which the picture will appear.


### -param hmf

TBD


### -param lprect

TBD




#### - hemf [in]

A handle to the enhanced metafile.


#### - lpRect [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the coordinates of the bounding rectangle used to display the picture. The coordinates are specified in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



When an application calls the <b>PlayEnhMetaFile</b> function, the system uses the picture frame in the enhanced-metafile header to map the picture onto the rectangle pointed to by the <i>lpRect</i> parameter. (This picture may be sheared or rotated by setting the world transform in the output device before calling <b>PlayEnhMetaFile</b>.) Points along the edges of the rectangle are included in the picture.

An enhanced-metafile picture can be clipped by defining the clipping region in the output device before playing the enhanced metafile.

If an enhanced metafile contains an optional palette, an application can achieve consistent colors by setting up a color palette on the output device before calling <b>PlayEnhMetaFile</b>. To retrieve the optional palette, use the <a href="https://msdn.microsoft.com/2d61fd6a-cebd-457e-ad00-d3e8bd15584a">GetEnhMetaFilePaletteEntries</a> function.

An enhanced metafile can be embedded in a newly created enhanced metafile by calling <b>PlayEnhMetaFile</b> and playing the source enhanced metafile into the device context for the new enhanced metafile.

The states of the output device context are preserved by this function. Any object created but not deleted in the enhanced metafile is deleted by this function.

To stop this function, an application can call the <a href="https://msdn.microsoft.com/1dcb3dfe-0ab0-4bf5-ac2f-7a9c11712eef">CancelDC</a> function from another thread to terminate the operation. In this case, the function returns <b>FALSE</b>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e4e5ef5c-d5ea-4931-bbec-1635e8f08c91">Opening an Enhanced Metafile and Displaying Its Contents</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1dcb3dfe-0ab0-4bf5-ac2f-7a9c11712eef">CancelDC</a>



<a href="https://msdn.microsoft.com/c42bcbe2-2e8f-42bd-a8e3-2827c6563300">GetEnhMetaFileHeader</a>



<a href="https://msdn.microsoft.com/2d61fd6a-cebd-457e-ad00-d3e8bd15584a">GetEnhMetaFilePaletteEntries</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>
 

 

