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

# TreeView_SetBorder macro


## -description


<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Sets the size of the border for the items in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/468b46ae-2ab2-4753-a0af-7c644f75ce62">TVM_SETBORDER</a> message explicitly.


## -parameters




### -param hwnd

TBD


### -param dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Action flags. This parameter can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVSBF_XBORDER"></a><a id="tvsbf_xborder"></a><dl>
<dt><b>TVSBF_XBORDER</b></dt>
</dl>
</td>
<td width="60%">
Applies the specified border size to the left side of the items in the tree-view control.

</td>
</tr>
<tr>
<td width="40%"><a id="TVSBF_YBORDER"></a><a id="tvsbf_yborder"></a><dl>
<dt><b>TVSBF_YBORDER</b></dt>
</dl>
</td>
<td width="60%">
Applies the specified border size to the top of the items in the tree-view control.

</td>
</tr>
</table>
 


### -param xBorder

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Size of the left border, in pixels. 


### -param yBorder

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Size of the top border, in pixels. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The item border is set just for spacing purposes. A successful setting triggers a recalculation of the scroll bars.




## -see-also




<a href="https://msdn.microsoft.com/468b46ae-2ab2-4753-a0af-7c644f75ce62">TVM_SETBORDER</a>
 

 

