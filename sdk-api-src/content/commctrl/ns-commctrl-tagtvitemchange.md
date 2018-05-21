---
UID: NS:commctrl.tagTVITEMCHANGE
title: tagTVITEMCHANGE
author: windows-driver-content
description: Contains information on a tree-view item change. This structure is sent with the TVN_ITEMCHANGED and TVN_ITEMCHANGING notifications.
old-location: controls\NMTVITEMCHANGE.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvitemchange.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: NMTVITEMCHANGE, NMTVITEMCHANGE structure [Windows Controls], _shell_NMTVITEMCHANGE, _shell_NMTVITEMCHANGE_cpp, commctrl/NMTVITEMCHANGE, controls.NMTVITEMCHANGE, controls._shell_NMTVITEMCHANGE, tagTVITEMCHANGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NMTVITEMCHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMTVITEMCHANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagTVITEMCHANGE structure


## -description


Contains information on a tree-view item change. This structure is sent with the <a href="https://msdn.microsoft.com/b09164bc-54da-457a-9fb7-3beab3dae3e4">TVN_ITEMCHANGED</a> and <a href="https://msdn.microsoft.com/c997871c-8eca-46c0-999d-2f6d7e3e6c96">TVN_ITEMCHANGING</a> notifications. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about the notification.


### -field uChanged

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the attribute. The only supported attribute is state. <b>uChanged</b> must have the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>TVIF_STATE</dt>
</dl>
</td>
<td width="60%">
The change is the state attribute.

</td>
</tr>
</table>
 


### -field hItem

Type: <b>HTREEITEM</b>

Handle to the changed tree-view item.


### -field uStateNew

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flag that specifies the new item state.


### -field uStateOld

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flag that specifies the item's previous state.


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Reserved for application specific data. For example, a value to associate with the item.

