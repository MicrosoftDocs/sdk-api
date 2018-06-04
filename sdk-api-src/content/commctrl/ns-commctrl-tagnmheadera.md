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

# tagNMHEADERA structure


## -description


Contains information about header control notification messages. This structure supersedes the 
			<b>HD_NOTIFY</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

A <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about the notification message. 


### -field iItem

Type: <b>int</b>

The zero-based index of the header item that is the focus of the notification message. 


### -field iButton

Type: <b>int</b>

A value specifying the index of the mouse button used to generate the notification message. This member can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Left button

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Right button

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Middle button

</td>
</tr>
</table>
 


### -field pitem

Type: <b><a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a>*</b>

An optional pointer to an <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure containing information about the item specified by 
					<b>iItem</b>. The 
					<b>mask</b> member of the <b>HDITEM</b> structure indicates which of its members are valid. 


## -remarks



While most header control notifications pass a pointer to an <b>NMHEADER</b> structure, only some of them use the <b>pitem</b> member to pass an <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure. Those that do use <b>pitem</b> may not provide complete information about the item. To obtain more information about an item, use <a href="https://msdn.microsoft.com/fb1330d3-fd28-490c-9caa-4b2b5ff86ba0">HDM_GETITEM</a>.



