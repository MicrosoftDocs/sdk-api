---
UID: NS:commctrl.tagNMKEY
title: tagNMKEY
author: windows-sdk-content
description: Contains information used with key notification messages.
old-location: controls\NMKEY.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\structures\nmkey.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPNMKEY, LPNMKEY, LPNMKEY structure pointer [Windows Controls], NMKEY, NMKEY structure [Windows Controls], _win32_NMKEY, _win32_NMKEY_cpp, commctrl/LPNMKEY, commctrl/NMKEY, controls.NMKEY, controls._win32_NMKEY, tagNMKEY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
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
 - Commctrl.h
api_name:
 - NMKEY
product: Windows
targetos: Windows
req.typenames: NMKEY, *LPNMKEY
req.redist: 
---

# tagNMKEY structure


## -description


Contains information used with key notification messages. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about this notification. 


### -field nVKey

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A virtual key code of the key that caused the event. 


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Flags associated with the key. These are the same flags that are passed in the high word of the 
					<i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> message.

