---
UID: NF:wingdi.DeleteEnhMetaFile
title: DeleteEnhMetaFile function
author: windows-sdk-content
description: The DeleteEnhMetaFile function deletes an enhanced-format metafile or an enhanced-format metafile handle.
old-location: gdi\deleteenhmetafile.htm
tech.root: gdi
ms.assetid: d3b93b3b-fa0b-4480-8348-19919c9e904d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteEnhMetaFile, DeleteEnhMetaFile function [Windows GDI], DeleteEnhMetaFileW, _win32_DeleteEnhMetaFile, gdi.deleteenhmetafile, wingdi/DeleteEnhMetaFile, wingdi/DeleteEnhMetaFileW
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteEnhMetaFileW (Unicode)
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
 - Ext-MS-Win-GDI-Metafile-l1-1-0.dll
 - Ext-MS-Win-GDI-Metafile-l1-1-1.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - DeleteEnhMetaFile
 - DeleteEnhMetaFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteEnhMetaFile function


## -description


The <b>DeleteEnhMetaFile</b> function deletes an enhanced-format metafile or an enhanced-format metafile handle.


## -parameters




### -param hmf [in]

A handle to an enhanced metafile.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If the <i>hemf</i> parameter identifies an enhanced metafile stored in memory, the <b>DeleteEnhMetaFile</b> function deletes the metafile. If <i>hemf</i> identifies a metafile stored on a disk, the function deletes the metafile handle but does not destroy the actual metafile. An application can retrieve the file by calling the <a href="https://msdn.microsoft.com/bcb9611e-8e4e-4f87-8a1e-dedbe0042821">GetEnhMetaFile</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e4e5ef5c-d5ea-4931-bbec-1635e8f08c91">Opening an Enhanced Metafile and Displaying Its Contents</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7c428828-b239-41d4-926c-88caa0aa7214">CopyEnhMetaFile</a>



<a href="https://msdn.microsoft.com/647f83ca-dca3-44af-a594-5f9ba2bd7607">CreateEnhMetaFile</a>



<a href="https://msdn.microsoft.com/bcb9611e-8e4e-4f87-8a1e-dedbe0042821">GetEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

