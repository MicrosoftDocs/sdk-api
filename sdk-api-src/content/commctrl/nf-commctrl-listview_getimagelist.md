---
UID: NF:commctrl.ListView_GetImageList
title: ListView_GetImageList macro
author: windows-sdk-content
description: Gets the handle to an image list used for drawing list-view items. You can use this macro or send the LVM_GETIMAGELIST message explicitly.
old-location: controls\ListView_GetImageList.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getimagelist.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: LVSIL_GROUPHEADER, LVSIL_NORMAL, LVSIL_SMALL, LVSIL_STATE, ListView_GetImageList, ListView_GetImageList macro [Windows Controls], _win32_ListView_GetImageList, _win32_ListView_GetImageList_cpp, commctrl/ListView_GetImageList, controls.ListView_GetImageList, controls._win32_ListView_GetImageList
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetImageList macro


## -description


Gets the handle to an image list used for drawing list-view items. You can use this macro or send the <a href="https://msdn.microsoft.com/dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0">LVM_GETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iImageList

Type: <b>int</b>

The image list to retrieve. This parameter can be one of the following values: 

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
 

