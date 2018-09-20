---
UID: NF:shobjidl_core.IEnumShellItems.Next
title: IEnumShellItems::Next
author: windows-sdk-content
description: Gets an array of one or more IShellItem interfaces from the enumeration.
old-location: shell\IEnumShellItems_Next.htm
tech.root: shell
ms.assetid: 8074ecea-30b9-4d1e-9184-457d3dd70bb8
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IEnumShellItems interface [Windows Shell],Next method, IEnumShellItems.Next, IEnumShellItems::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumShellItems interface, _shell_IEnumShellItems_Next, shell.IEnumShellItems_Next, shobjidl_core/IEnumShellItems::Next
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
 - IEnumShellItems.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumShellItems::Next


## -description


Gets an array of one or more <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces from the enumeration.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements in the array referenced by the <i>rgelt</i> parameter.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

The address of an array of pointers to <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces that receive the enumerated item or items. The calling application is responsible for freeing the <b>IShellItem</b> interfaces by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to a value that receives the number of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces successfully retrieved. The count can be smaller than the value specified in the <i>celt</i> parameter. This parameter can be <b>NULL</b> on entry only if <i>celt</i> is one, because in that case the method can only retrieve one item and return <b>S_OK</b>, or zero items and return <b>S_FALSE</b>.



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
if at least <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface was retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
 if there are no more <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces in the enumeration.

</td>
</tr>
<tr>
<td width="40%">
</td>
<td width="60%">
Returns an  error value if the function fails for any other reason.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

