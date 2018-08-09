---
UID: NF:wingdi.DeleteMetaFile
title: DeleteMetaFile function
author: windows-sdk-content
description: The DeleteMetaFile function deletes a Windows-format metafile or Windows-format metafile handle.
old-location: gdi\deletemetafile.htm
old-project: gdi
ms.assetid: 51766282-f185-4e29-a36e-1069d9d61f7c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DeleteMetaFile, DeleteMetaFile function [Windows GDI], _win32_DeleteMetaFile, gdi.deletemetafile, wingdi/DeleteMetaFile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
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
 - DeleteMetaFile
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteMetaFile function


## -description


The <b>DeleteMetaFile</b> function deletes a Windows-format metafile or Windows-format metafile handle.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>.</div><div> </div>

## -parameters




### -param hmf [in]

A handle to a Windows-format metafile.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If the metafile identified by the <i>hmf</i> parameter is stored in memory (rather than on a disk), its content is lost when it is deleted by using the <b>DeleteMetaFile</b> function.




## -see-also




<a href="https://msdn.microsoft.com/e9f97591-697b-47d0-a748-60fda4d5258c">CopyMetaFile</a>



<a href="https://msdn.microsoft.com/81b3baae-f0e6-4b71-a6de-953ad3376dbd">CreateMetaFile</a>



<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

