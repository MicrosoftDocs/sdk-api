---
UID: NS:commctrl.tagNMLVODSTATECHANGE
title: tagNMLVODSTATECHANGE
author: windows-sdk-content
description: Structure that contains information for use in processing the LVN_ODSTATECHANGED notification code.
old-location: controls\NMLVODSTATECHANGE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvodstatechange.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
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


Structure that contains information for use in processing the <a href="https://msdn.microsoft.com/a3aafda5-a3ec-4f84-8153-8d34097e04f1">LVN_ODSTATECHANGED</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field iFrom

Type: <b>int</b>

Zero-based index of the first item in the range of items. 


### -field iTo

Type: <b>int</b>

Zero-based index of the last item in the range of items. 


### -field uNewState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Value indicating the new state for the item or items. This member can be any valid combination of the <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">list-view item states</a>. 


### -field uOldState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Value indicating the old state for the item or items. This member can be any valid combination of the <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">list-view item states</a>. 

