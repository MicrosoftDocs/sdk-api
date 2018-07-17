---
UID: NF:commctrl.ListView_SetImageList
title: ListView_SetImageList macro
author: windows-sdk-content
description: Assigns an image list to a list-view control. You can use this macro or send the LVM_SETIMAGELIST message explicitly.
old-location: controls\ListView_SetImageList.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setimagelist.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: LVSIL_GROUPHEADER, LVSIL_NORMAL, LVSIL_SMALL, LVSIL_STATE, ListView_SetImageList, ListView_SetImageList macro [Windows Controls], _win32_ListView_SetImageList, _win32_ListView_SetImageList_cpp, commctrl/ListView_SetImageList, controls.ListView_SetImageList, controls._win32_ListView_SetImageList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_SetImageList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetImageList macro


## -description


Assigns an image list to a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761178(v=VS.85).aspx">LVM_SETIMAGELIST</a> message explicitly. 


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



The current image list will be destroyed when the list-view control is destroyed unless the <a href="https://msdn.microsoft.com/library/Bb774739(v=VS.85).aspx">LVS_SHAREIMAGELISTS</a> style is set. If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.



