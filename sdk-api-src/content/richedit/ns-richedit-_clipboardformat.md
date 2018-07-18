---
UID: NS:richedit._clipboardformat
title: "_clipboardformat"
author: windows-sdk-content
description: Specifies the clipboard format. This structure included with the EN_CLIPFORMAT notification.
old-location: controls\clipboardformat.htm
old-project: controls
ms.assetid: 5AD870B6-C4F1-446C-A516-171B24355EFA
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CLIPBOARDFORMAT, CLIPBOARDFORMAT structure [Windows Controls], _clipboardformat, controls.clipboardformat, richedit/CLIPBOARDFORMAT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CLIPBOARDFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - CLIPBOARDFORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _clipboardformat structure


## -description


Specifies the clipboard format. This structure included with the <a href="https://msdn.microsoft.com/79FE1350-4D45-447B-B705-63E966AC7F0E">EN_CLIPFORMAT</a> notification. 



## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

Structure that contains information about this notification message.


### -field cf

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A clipboard format registered by a call to the <a href="https://msdn.microsoft.com/892add91-a937-4602-86d2-5e5550a81872">RegisterClipboardFormat</a> function. 



## -see-also




<a href="https://msdn.microsoft.com/79FE1350-4D45-447B-B705-63E966AC7F0E">EN_CLIPFORMAT</a>
 

 

