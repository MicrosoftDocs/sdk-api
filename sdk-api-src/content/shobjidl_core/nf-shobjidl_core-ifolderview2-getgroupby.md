---
UID: NF:shobjidl_core.IFolderView2.GetGroupBy
title: IFolderView2::GetGroupBy
author: windows-sdk-content
description: Retrieves the property and sort order used for grouping items in the folder display.
old-location: shell\IFolderView2_GetGroupBy.htm
tech.root: shell
ms.assetid: 6fabf321-34af-4a5e-b2c0-9ed344e1c782
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetGroupBy, GetGroupBy method [Windows Shell], GetGroupBy method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetGroupBy method, IFolderView2.GetGroupBy, IFolderView2::GetGroupBy, _shell_IFolderView2_GetGroupBy, shell.IFolderView2_GetGroupBy, shobjidl_core/IFolderView2::GetGroupBy
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
 - IFolderView2.GetGroupBy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView2::GetGroupBy


## -description


Retrieves the property and sort order used for grouping items in the folder display.


## -parameters




### -param pkey [out]

Type: <b><a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> by which the view is grouped.


### -param pfAscending [out]

Type: <b>BOOL*</b>

A pointer to a value of type <b>BOOL</b> that indicates sort order of the groups.


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
The view is grouped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The view is not grouped.

</td>
</tr>
</table>
 



