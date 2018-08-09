---
UID: NF:shobjidl_core.IFolderView2.GetItem
title: IFolderView2::GetItem
author: windows-sdk-content
description: Retrieves an object that represents a specified item.
old-location: shell\IFolderView2_GetItem.htm
old-project: shell
ms.assetid: 557ff412-2da9-4723-9f84-802e084ebaca
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetItem, GetItem method [Windows Shell], GetItem method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetItem method, IFolderView2.GetItem, IFolderView2::GetItem, _shell_IFolderView2_GetItem, shell.IFolderView2_GetItem, shobjidl_core/IFolderView2::GetItem
ms.prod: windows
ms.technology: windows-sdk
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
 - IFolderView2.GetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView2::GetItem


## -description


Retrieves an object that represents a specified item.


## -parameters




### -param iItem [in]

Type: <b>int</b>

The zero-based index of the item to retrieve.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID to represent the item, such as IID_IShellItem.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the specified item was found, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The index in <i>iItem</i> is out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/52fcf0df-f532-4114-b1c9-96838f1a5e77">IFolderView2</a>



<a href="https://msdn.microsoft.com/fca9fd45-05ce-4300-aecf-a2843614a11d">IFolderView2::GetSelectedItem</a>
 

 

