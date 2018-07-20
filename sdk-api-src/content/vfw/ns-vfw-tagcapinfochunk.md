---
UID: NS:vfw.tagCapInfoChunk
title: tagCapInfoChunk
author: windows-sdk-content
description: The CAPINFOCHUNK structure contains parameters that can be used to define an information chunk within an AVI capture file. The WM_CAP_FILE_SET_INFOCHUNK message or capSetInfoChunk macro is used to send a CAPINFOCHUNK structure to a capture window.
old-location: multimedia\capinfochunk.htm
old-project: Multimedia
ms.assetid: 7dbe8209-73c3-4eab-965e-91b94f77f0a7
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: "*LPCAPINFOCHUNK, *PCAPINFOCHUNK, CAPINFOCHUNK, CAPINFOCHUNK structure [Windows Multimedia], _win32_CAPINFOCHUNK_str, multimedia.capinfochunk, tagCapInfoChunk, vfw/CAPINFOCHUNK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CAPINFOCHUNK, *PCAPINFOCHUNK, *LPCAPINFOCHUNK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - CAPINFOCHUNK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# tagCapInfoChunk structure


## -description



The <b>CAPINFOCHUNK</b> structure contains parameters that can be used to define an information chunk within an AVI capture file. The <a href="https://msdn.microsoft.com/67d11a05-a2b4-45d2-ba66-83a198745303">WM_CAP_FILE_SET_INFOCHUNK</a> message or <b>capSetInfoChunk</b> macro is used to send a <b>CAPINFOCHUNK</b> structure to a capture window.




## -struct-fields




### -field fccInfoID

Four-character code that identifies the representation of the chunk data. If this value is <b>NULL</b> and <b>lpData</b> is <b>NULL</b>, all accumulated information chunks are deleted.


### -field lpData

Pointer to the data. If this value is <b>NULL</b>, all <b>fccInfoID</b> information chunks are deleted.


### -field cbData

Size, in bytes, of the data pointed to by <b>lpData</b>. If <b>lpData</b> specifies a null-terminated string, use the string length incremented by one to save the <b>NULL</b> with the string.


## -see-also




Video Capture



<a href="https://msdn.microsoft.com/180010d2-240e-433d-b306-341b9b1e0b57">Video Capture Structures</a>



<a href="https://msdn.microsoft.com/67d11a05-a2b4-45d2-ba66-83a198745303">WM_CAP_FILE_SET_INFOCHUNK</a>
 

 

