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

# NMTBDISPINFOW structure


## -description


Contains and receives display information for a toolbar item. This structure is used with the <a href="https://msdn.microsoft.com/ed6e4141-2bf8-4a92-8349-f3833c87fcf3">TBN_GETDISPINFO</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Set of flags that indicate which members of this structure are being requested. This can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TBNF_IMAGE"></a><a id="tbnf_image"></a><dl>
<dt><b>TBNF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The item's image index is being requested. The image index must be placed in the 
						<b>iImage</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="TBNF_TEXT"></a><a id="tbnf_text"></a><dl>
<dt><b>TBNF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="TBNF_DI_SETITEM"></a><a id="tbnf_di_setitem"></a><dl>
<dt><b>TBNF_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">
Set this flag when processing <a href="https://msdn.microsoft.com/ed6e4141-2bf8-4a92-8349-f3833c87fcf3">TBN_GETDISPINFO</a>; the toolbar control will retain the supplied information and not request it again.

</td>
</tr>
</table>
 


### -field idCommand

Type: <b>int</b>

Command identifier of the item for which display information is being requested. This member is filled in by the control before it sends the notification code. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD_PTR</a></b>

Application-defined value associated with the item for which display information is being requested. This member is filled in by the control before sending the notification code. 


### -field iImage

Type: <b>int</b>

Image index for the item. 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to a character buffer that receives the item's text. 


### -field cchText

Type: <b>int</b>

Size of the 
					<b>pszText</b> buffer, in characters. 

