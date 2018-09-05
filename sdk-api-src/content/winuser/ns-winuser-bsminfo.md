---
UID: NS:winuser.BSMINFO
title: BSMINFO
author: windows-sdk-content
description: Contains information about a window that denied a request from BroadcastSystemMessageEx.
old-location: winmsg\bsminfo.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messageandmessagequeuestructures\bsminfo.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PBSMINFO, BSMINFO, BSMINFO structure [Windows and Messages], PBSMINFO, PBSMINFO structure pointer [Windows and Messages], _win32_BSMINFO_str, _win32_bsminfo_str_cpp, winmsg.bsminfo, winui._win32_bsminfo_str, winuser/BSMINFO, winuser/PBSMINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: BSMINFO, *PBSMINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - BSMINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# BSMINFO structure


## -description


Contains information about a window that denied a request from <a href="https://msdn.microsoft.com/bfc9f836-7960-4249-98c9-1c73b7641f77">BroadcastSystemMessageEx</a>. 


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size, in bytes, of this structure. 


### -field hdesk

Type: <b>HDESK</b>

A desktop handle to the window specified by 
					<b>hwnd</b>. This value is returned only if <a href="https://msdn.microsoft.com/bfc9f836-7960-4249-98c9-1c73b7641f77">BroadcastSystemMessageEx</a> specifies <b>BSF_RETURNHDESK</b> and <b>BSF_QUERY</b>. 


### -field hwnd

Type: <b>HWND</b>

A handle to the window that denied the request. This value is returned if <a href="https://msdn.microsoft.com/bfc9f836-7960-4249-98c9-1c73b7641f77">BroadcastSystemMessageEx</a> specifies <b>BSF_QUERY</b>. 


### -field luid

Type: <b>LUID</b>

A locally unique identifier (LUID) for the window. 


## -see-also




<a href="https://msdn.microsoft.com/bfc9f836-7960-4249-98c9-1c73b7641f77">BroadcastSystemMessageEx</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<b>Reference</b>
 

 

