---
UID: NF:shobjidl_core.IFolderView2.GetSelection
title: IFolderView2::GetSelection
author: windows-sdk-content
description: Gets the current selection as an IShellItemArray.
old-location: shell\IFolderView2_GetSelection.htm
tech.root: shell
ms.assetid: d8ff0c8f-9678-455b-b7ec-9b651df769bc
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetSelection, GetSelection method [Windows Shell], GetSelection method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetSelection method, IFolderView2.GetSelection, IFolderView2::GetSelection, _shell_IFolderView2_GetSelection, shell.IFolderView2_GetSelection, shobjidl_core/IFolderView2::GetSelection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.GetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView2::GetSelection


## -description


Gets the current selection as an IShellItemArray.


## -parameters




### -param fNoneImpliesFolder [in]

Type: <b>BOOL</b>

If <b>TRUE</b>, this method returns an IShellItemArray containing the parent folder when there is no current selection.


### -param ppsia [out]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>**</b>

The address of a pointer to an IShellItemArray.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values, or an error otherwise.

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The IShellItemArray returned has zero items.

</td>
</tr>
</table>
 



