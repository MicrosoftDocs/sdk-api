---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ListView_SetExtendedListViewStyle macro


## -description


Sets extended styles for list-view controls. You can use this macro or send the <a href="https://msdn.microsoft.com/eb3f47ed-484a-49a8-94b0-e50ee081bd69">LVM_SETEXTENDEDLISTVIEWSTYLE</a> message explicitly.


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control that will receive the style change. 


### -param dw

TBD






#### - dwExStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A <b>DWORD</b> value that specifies the extended list-view control style. This parameter can be a combination of <a href="https://msdn.microsoft.com/f53daacc-aa17-4652-8fef-8bfb749fae09">Extended List-View Styles</a>. 


## -remarks



For backward compatibility reasons, the <b>ListView_SetExtendedListViewStyle</b> macro has not been updated to use 
<i>dwExMask</i>. To use the <i>dwExMask</i>
value, use the <a href="https://msdn.microsoft.com/1beb06dc-060b-40d8-969c-fb0dfeac2861">ListView_SetExtendedListViewStyleEx</a> macro. 

When you use this macro to set the <a href="Extended_list_view_styles.htm">LVS_EX_CHECKBOXES</a> style, any previously set state image index will be discarded. All check boxes will be initialized to the unchecked state. The state image index is contained in bits 12 through 15 of the 
<b>state</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure.



