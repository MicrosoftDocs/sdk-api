---
UID: NF:shobjidl_core.IFolderView2.GetVisibleItem
title: IFolderView2::GetVisibleItem
author: windows-sdk-content
description: Gets the next visible item in relation to a given index in the view.
old-location: shell\IFolderView2_GetVisibleItem.htm
old-project: shell
ms.assetid: 5b196377-53c4-49a1-be35-39d34b1638e3
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetVisibleItem, GetVisibleItem method [Windows Shell], GetVisibleItem method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetVisibleItem method, IFolderView2.GetVisibleItem, IFolderView2::GetVisibleItem, _shell_IFolderView2_GetVisibleItem, shell.IFolderView2_GetVisibleItem, shobjidl_core/IFolderView2::GetVisibleItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.GetVisibleItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView2::GetVisibleItem


## -description


Gets the next visible item in relation to a given index in the view.


## -parameters




### -param iStart [in]

Type: <b>int</b>

The zero-based position at which to start searching for a visible item.


### -param fPrevious [in]

Type: <b>BOOL</b>

<b>TRUE</b> to find the first visible item before <i>iStart</i>. <b>FALSE</b> to find the first visible item after <i>iStart</i>.


### -param piItem [out]

Type: <b>int*</b>

When this method returns, contains a pointer to a value that receives the index of the visible item in the view.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Item retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Item not found. Note that this is a success code.

</td>
</tr>
</table>
 



