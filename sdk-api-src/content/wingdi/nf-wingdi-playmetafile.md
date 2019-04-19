---
UID: NF:wingdi.PlayMetaFile
title: PlayMetaFile function (wingdi.h)
author: windows-sdk-content
description: The PlayMetaFile function displays the picture stored in the given Windows-format metafile on the specified device.
old-location: gdi\playmetafile.htm
tech.root: gdi
ms.assetid: 044894df-dc8a-41b2-8810-e0a1b8bc19d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PlayMetaFile, PlayMetaFile function [Windows GDI], _win32_PlayMetaFile, gdi.playmetafile, wingdi/PlayMetaFile
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
 - Ext-MS-Win-GDI-Metafile-L1-1-2.dll
 - GDI32Full.dll
api_name:
 - PlayMetaFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PlayMetaFile function


## -description


The <b>PlayMetaFile</b> function displays the picture stored in the given Windows-format metafile on the specified device.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>.</div><div> </div>

## -parameters




### -param hdc [in]

Handle to a device context.


### -param hmf [in]

Handle to a Windows-format metafile.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



To convert a Windows-format metafile into an enhanced format metafile, use the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function.

A Windows-format metafile can be played multiple times.

A Windows-format metafile can be embedded in a second Windows-format metafile by calling the <b>PlayMetaFile</b> function and playing the source metafile into the device context for the target metafile.

Any object created but not deleted in the Windows-format metafile is deleted by this function.

To stop this function, an application can call the <a href="https://msdn.microsoft.com/1dcb3dfe-0ab0-4bf5-ac2f-7a9c11712eef">CancelDC</a> function from another thread to terminate the operation. In this case, the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dcb3dfe-0ab0-4bf5-ac2f-7a9c11712eef">CancelDC</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 

