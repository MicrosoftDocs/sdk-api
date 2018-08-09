---
UID: NF:shobjidl_core.IShellItem.Compare
title: IShellItem::Compare
author: windows-sdk-content
description: Compares two IShellItem objects.
old-location: shell\IShellItem_Compare.htm
old-project: shell
ms.assetid: 737a93e0-2e27-466b-889c-04a25e52e883
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Compare, Compare method [Windows Shell], Compare method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],Compare method, IShellItem.Compare, IShellItem::Compare, _win32_IShellItem_Compare, shell.IShellItem_Compare, shobjidl_core/IShellItem::Compare
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellItem.Compare
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem::Compare


## -description


Compares two <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> objects.


## -parameters




### -param psi

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object to compare with the existing <b>IShellItem</b> object.


### -param hint

Type: <b><a href="https://msdn.microsoft.com/4d333302-5be3-4e8d-9018-e42729df0cc3">SICHINTF</a></b>

One of the <a href="https://msdn.microsoft.com/4d333302-5be3-4e8d-9018-e42729df0cc3">SICHINTF</a> values that determines how to perform the comparison. See <b>SICHINTF</b> for the list of possible values for this parameter.


### -param piOrder

Type: <b>int*</b>

This parameter receives the result of the comparison. If the two items are the same this parameter equals zero; if they are different the parameter is nonzero.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the items are the same, S_FALSE if they are different, or an error value otherwise.




## -remarks



The data type used in the second parameter, SICHINTF, is defined as: 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef DWORD SICHINTF;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

