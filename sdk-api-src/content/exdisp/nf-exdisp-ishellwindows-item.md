---
UID: NF:exdisp.IShellWindows.Item
title: IShellWindows::Item
author: windows-sdk-content
description: Returns the registered Shell window for a specified index.
old-location: shell\IShellWindows_Item.htm
tech.root: shell
ms.assetid: 04157d1a-8a4d-4ffd-882d-41748408ba2b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IShellWindows interface [Windows Shell],Item method, IShellWindows.Item, IShellWindows::Item, Item, Item method [Windows Shell], Item method [Windows Shell],IShellWindows interface, _win32_IShellWindows_Item, exdisp/IShellWindows::Item, shell.IShellWindows_Item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
---

# IShellWindows::Item


## -description


Returns the registered Shell window for a specified index.


## -parameters




### -param index [in, optional]

Type: <b>VARIANT</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> of type VT_UI4, VT_I2, or VT_I4. If the type is VT_UI4, the value of <i>index</i> is interpreted as a member of <a href="https://msdn.microsoft.com/79d4fcf3-5256-4e21-ab9a-94605e1d742f">ShellWindowTypeConstants</a>; in this case, <b>Item</b> returns the window that is closest to the foreground window and has a matching type. If the type is VT_I, or VT_I4, <i>index</i> is treated as an index into the Shell windows collection.


### -param Folder [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>**</b>

A reference to the window's <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface, or <b>NULL</b> if the specified window was not found.


## -returns



Type: <b>HRESULT</b>

One of the following values, or a standard result code.

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
The specified window was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified window was not found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/e91b2be7-2be9-4460-9a2a-57090dcfc961">IShellWindows::_NewEnum</a>



<a href="https://msdn.microsoft.com/50781569-4c80-4304-96f3-8a135cea3b20">IShellWindows::get_Count</a>
 

 

