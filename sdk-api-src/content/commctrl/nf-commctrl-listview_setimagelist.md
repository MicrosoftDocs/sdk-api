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

# ListView_SetImageList macro


## -description


Assigns an image list to a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/5241065b-85e4-412e-9868-fd5b15ff7c17">LVM_SETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list to assign. 


### -param iImageList

Type: <b>int</b>

The type of image list. This parameter can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVSIL_NORMAL"></a><a id="lvsil_normal"></a><dl>
<dt><b>LVSIL_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Image list with large icons.

</td>
</tr>
<tr>
<td width="40%"><a id="LVSIL_SMALL"></a><a id="lvsil_small"></a><dl>
<dt><b>LVSIL_SMALL</b></dt>
</dl>
</td>
<td width="60%">
Image list with small icons.

</td>
</tr>
<tr>
<td width="40%"><a id="LVSIL_STATE"></a><a id="lvsil_state"></a><dl>
<dt><b>LVSIL_STATE</b></dt>
</dl>
</td>
<td width="60%">
Image list with state images.

</td>
</tr>
<tr>
<td width="40%"><a id="LVSIL_GROUPHEADER"></a><a id="lvsil_groupheader"></a><dl>
<dt><b>LVSIL_GROUPHEADER</b></dt>
</dl>
</td>
<td width="60%">
Image list for group header.

</td>
</tr>
</table>
 


## -remarks



The current image list will be destroyed when the list-view control is destroyed unless the <a href="List_view_window_styles.htm">LVS_SHAREIMAGELISTS</a> style is set. If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.



