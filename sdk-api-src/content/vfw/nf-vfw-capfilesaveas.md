---
UID: NF:vfw.capFileSaveAs
title: capFileSaveAs macro
author: windows-sdk-content
description: The capFileSaveAs macro copies the contents of the capture file to another file. You can use this macro or explicitly call the WM_CAP_FILE_SAVEAS message.
old-location: multimedia\capfilesaveas.htm
tech.root: Multimedia
ms.assetid: 164bb345-c092-4adb-8f0f-83e31d36390f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_capFileSaveAs, capFileSaveAs, capFileSaveAs macro [Windows Multimedia], multimedia.capfilesaveas, vfw/capFileSaveAs"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capFileSaveAs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capFileSaveAs macro


## -description



The <b>capFileSaveAs</b> macro copies the contents of the capture file to another file. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/fab37bee-3160-4ebc-b58f-46021ed49b55">WM_CAP_FILE_SAVEAS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to the null-terminated string that contains the name of the destination file used to copy the file. 


## -remarks



This message does not change the name or contents of the current capture file.

If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.

Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data. This message copies only the portion of the file containing the capture data.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

