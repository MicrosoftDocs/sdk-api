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

# tagLVDISPINFOW structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/04310e39-69bc-45d7-958c-00452279d7a9">LVN_GETDISPINFO</a> or <a href="https://msdn.microsoft.com/1ea51d50-4a57-4662-972e-89e916fa9b16">LVN_SETDISPINFO</a> notification code. This structure is the same as the <b>LV_DISPINFO</b> structure, but has been renamed to fit standard naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification code. 


### -field item

Type: <b><a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a></b>


<a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure that identifies the item or subitem. The structure either contains or receives information about the item. The <b>mask</b> member contains a set of bit flags that specify which item attributes are relevant.
For more information on the available bit flags, see <b>LVITEM</b>.


## -remarks




		If the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure is receiving item text, the <b>pszText</b> and <b>cchTextMax</b> members specify the address and size of a buffer. You can either copy text to the buffer or assign the address of a string to the <b>pszText</b> member. In the latter case, you must not change or delete the string until the corresponding item text is deleted or two additional <a href="https://msdn.microsoft.com/04310e39-69bc-45d7-958c-00452279d7a9">LVN_GETDISPINFO</a> messages have been sent. 



If you are handling the <a href="https://msdn.microsoft.com/04310e39-69bc-45d7-958c-00452279d7a9">LVN_GETDISPINFO</a> message, you can set the LVIF_DI_SETITEM flag in the <b>mask</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure. This tells the operating system to store the requested list item information and not ask for it again. For list-view controls with the <a href="List_view_window_styles.htm">LVS_REPORT</a> style, this flag only applies to the first (subitem 0) column's information. The control will not store information for subitems.
		



