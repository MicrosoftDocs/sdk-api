---
UID: NF:wingdi.PlayEnhMetaFile
title: PlayEnhMetaFile function (wingdi.h)
author: windows-sdk-content
description: The PlayEnhMetaFile function displays the picture stored in the specified enhanced-format metafile.
old-location: gdi\playenhmetafile.htm
tech.root: gdi
ms.assetid: 51e8937b-0c42-49fe-8930-7af303fce788
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PlayEnhMetaFile, PlayEnhMetaFile function [Windows GDI], _win32_PlayEnhMetaFile, gdi.playenhmetafile, wingdi/PlayEnhMetaFile
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - PlayEnhMetaFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PlayEnhMetaFile function


## -description


The <b>PlayEnhMetaFile</b> function displays the picture stored in the specified enhanced-format metafile.


## -parameters




### -param hdc [in]

A handle to the device context for the output device on which the picture will appear.


### -param hmf [in]

A handle to the enhanced metafile.


### -param lprect [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the coordinates of the bounding rectangle used to display the picture. The coordinates are specified in logical units.


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



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>
 

 

