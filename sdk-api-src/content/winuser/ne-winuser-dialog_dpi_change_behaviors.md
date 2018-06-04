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

# DIALOG_DPI_CHANGE_BEHAVIORS enumeration


## -description


In <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">Per Monitor v2 contexts</a>, dialogs will automatically respond to DPI changes by resizing themselves and re-computing the positions of their child windows (here referred to as re-layouting). This enum works in conjunction with <a href="https://msdn.microsoft.com/48A13F57-9D82-4F79-962B-FBD02FFF9B39">SetDialogDpiChangeBehavior</a> in order to override the default DPI scaling behavior for dialogs.

This does not affect DPI scaling behavior for the child windows of dialogs (beyond re-layouting), which is controlled by <a href="https://msdn.microsoft.com/B368D997-F409-491A-8578-004C7408A160">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>.


## -enum-fields




### -field DDC_DEFAULT

The default behavior of the dialog manager. In response to a DPI change, the dialog manager will re-layout each control, update the font on each control, resize the dialog, and update the dialog's own font.


### -field DDC_DISABLE_ALL

Prevents the dialog manager from responding to <a href="https://msdn.microsoft.com/038CAA21-0944-45D3-8C40-A6498F36D9E4">WM_GETDPISCALEDSIZE</a> and <a href="https://msdn.microsoft.com/97C458F2-89CD-45FF-ABEE-F158A3BCE0B8">WM_DPICHANGED</a>, disabling all default DPI scaling behavior.


### -field DDC_DISABLE_RESIZE

Prevents the dialog manager from resizing the dialog in response to a DPI change.


### -field DDC_DISABLE_CONTROL_RELAYOUT

Prevents the dialog manager from re-layouting all of the dialogue's immediate children HWNDs in response to a DPI change.


## -see-also




<a href="https://msdn.microsoft.com/B368D997-F409-491A-8578-004C7408A160">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/8ED61C77-36C8-453B-BAB1-505CE4974D63">GetDialogDpiChangeBehavior</a>



<a href="https://msdn.microsoft.com/48A13F57-9D82-4F79-962B-FBD02FFF9B39">SetDialogDpiChangeBehavior</a>
 

 

