---
UID: NF:vfw.capFileSetInfoChunk
title: capFileSetInfoChunk macro
author: windows-sdk-content
description: The capFileSetInfoChunk macro sets and clears information chunks. Information chunks can be inserted in an AVI file during capture to embed text strings or custom data. You can use this macro or explicitly call the WM_CAP_FILE_SET_INFOCHUNK message.
old-location: multimedia\capfilesetinfochunk.htm
tech.root: Multimedia
ms.assetid: b0772aa7-944c-450e-a703-0057a3230cb0
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "_win32_capFileSetInfoChunk, capFileSetInfoChunk, capFileSetInfoChunk macro [Windows Multimedia], multimedia.capfilesetinfochunk, vfw/capFileSetInfoChunk"
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
 - capFileSetInfoChunk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capFileSetInfoChunk macro


## -description



The <b>capFileSetInfoChunk</b> macro sets and clears information chunks. Information chunks can be inserted in an AVI file during capture to embed text strings or custom data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/67d11a05-a2b4-45d2-ba66-83a198745303">WM_CAP_FILE_SET_INFOCHUNK</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param lpInfoChunk

Pointer to a CAPINFOCHUNK structure defining the information chunk to be created or deleted. 


## -remarks



Multiple registered information chunks can be added to an AVI file. After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared. To clear a single entry, specify the information chunk in the <b>fccInfoID</b> member and <b>NULL</b> in the <b>lpData</b> member of the <a href="https://msdn.microsoft.com/7dbe8209-73c3-4eab-965e-91b94f77f0a7">CAPINFOCHUNK</a> structure. To clear all entries, specify <b>NULL</b> in <b>fccInfoID</b>.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

