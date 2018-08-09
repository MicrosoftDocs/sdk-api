---
UID: NS:commctrl.tagLVDISPINFO
title: tagLVDISPINFO
author: windows-sdk-content
description: Contains information about an LVN_GETDISPINFO or LVN_SETDISPINFO notification code. This structure is the same as the LV_DISPINFO structure, but has been renamed to fit standard naming conventions.
old-location: controls\NMLVDISPINFO.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvdispinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPNMLVDISPINFOA, NMLVDISPINFO, NMLVDISPINFO structure [Windows Controls], NMLVDISPINFOA, NMLVDISPINFOW, _win32_NMLVDISPINFO, _win32_NMLVDISPINFO_cpp, commctrl/NMLVDISPINFO, commctrl/NMLVDISPINFOA, commctrl/NMLVDISPINFOW, controls.NMLVDISPINFO, controls._win32_NMLVDISPINFO, tagLVDISPINFO"
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
req.unicode-ansi: NMLVDISPINFOW (Unicode) and NMLVDISPINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NMLVDISPINFOA, *LPNMLVDISPINFOA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMLVDISPINFO
 - NMLVDISPINFOA
 - NMLVDISPINFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagLVDISPINFO structure


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
		



