---
UID: NS:commctrl.tagNMLVODSTATECHANGE
title: tagNMLVODSTATECHANGE
author: windows-sdk-content
description: Structure that contains information for use in processing the LVN_ODSTATECHANGED notification code.
old-location: controls\NMLVODSTATECHANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvodstatechange.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPNMLVODSTATECHANGE, LPNMLVODSTATECHANGE, LPNMLVODSTATECHANGE structure pointer [Windows Controls], NMLVODSTATECHANGE, NMLVODSTATECHANGE structure [Windows Controls], _win32_NMLVODSTATECHANGE, _win32_NMLVODSTATECHANGE_cpp, commctrl/LPNMLVODSTATECHANGE, commctrl/NMLVODSTATECHANGE, controls.NMLVODSTATECHANGE, controls._win32_NMLVODSTATECHANGE, tagNMLVODSTATECHANGE"
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
 - NMLVODSTATECHANGE
product: Windows
targetos: Windows
req.typenames: NMLVODSTATECHANGE, *LPNMLVODSTATECHANGE
req.redist: 
---

# tagNMLVODSTATECHANGE structure


## -description


Structure that contains information for use in processing the <a href="https://msdn.microsoft.com/en-us/library/Bb774859(v=VS.85).aspx">LVN_ODSTATECHANGED</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field iFrom

Type: <b>int</b>

Zero-based index of the first item in the range of items. 


### -field iTo

Type: <b>int</b>

Zero-based index of the last item in the range of items. 


### -field uNewState

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Value indicating the new state for the item or items. This member can be any valid combination of the <a href="https://msdn.microsoft.com/en-us/library/Bb774733(v=VS.85).aspx">list-view item states</a>. 


### -field uOldState

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Value indicating the old state for the item or items. This member can be any valid combination of the <a href="https://msdn.microsoft.com/en-us/library/Bb774733(v=VS.85).aspx">list-view item states</a>. 

