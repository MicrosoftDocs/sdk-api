---
UID: NS:richedit._reqresize
title: "_reqresize"
author: windows-sdk-content
description: Contains the requested size of a rich edit control. A rich edit control sends this structure to its parent window as part of an EN_REQUESTRESIZE notification code.
old-location: controls\REQRESIZE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\reqresize.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: REQRESIZE, REQRESIZE structure [Windows Controls], _reqresize, _win32_REQRESIZE_str, _win32_REQRESIZE_str_cpp, controls.REQRESIZE, controls._win32_REQRESIZE_str, richedit/REQRESIZE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Richedit.h
api_name:
 - REQRESIZE
product: Windows
targetos: Windows
req.typenames: REQRESIZE
req.redist: 
---

# _reqresize structure


## -description


Contains the requested size of a rich edit control. A rich edit control sends this structure to its parent window as part of an <a href="https://msdn.microsoft.com/708c23b1-7b81-46f1-9595-46230693855d">EN_REQUESTRESIZE</a> notification code.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

Notification header. 


### -field rc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

Requested new size. 


## -see-also




<a href="https://msdn.microsoft.com/708c23b1-7b81-46f1-9595-46230693855d">EN_REQUESTRESIZE</a>
 

 

