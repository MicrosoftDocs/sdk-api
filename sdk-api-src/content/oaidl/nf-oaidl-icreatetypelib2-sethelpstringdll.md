---
UID: NF:oaidl.ICreateTypeLib2.SetHelpStringDll
title: ICreateTypeLib2::SetHelpStringDll
author: windows-sdk-content
description: Sets the DLL name to be used for Help string lookup (for localization purposes).
old-location: automat\icreatetypelib2_sethelpstringdll.htm
tech.root: automat
ms.assetid: f00a3dbf-7205-48fd-abeb-1d2d80be7743
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICreateTypeLib2 interface [Automation],SetHelpStringDll method, ICreateTypeLib2.SetHelpStringDll, ICreateTypeLib2::SetHelpStringDll, SetHelpStringDll, SetHelpStringDll method [Automation], SetHelpStringDll method [Automation],ICreateTypeLib2 interface, _oa96_ICreateTypeLib2_SetHelpStringDll, automat.icreatetypelib2_sethelpstringdll, oaidl/ICreateTypeLib2::SetHelpStringDll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - oaidl.h
api_name:
 - ICreateTypeLib2.SetHelpStringDll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateTypeLib2::SetHelpStringDll


## -description


Sets the DLL name to be used for Help string lookup (for localization purposes).


## -parameters




### -param szFileName [in]

The DLL file name.


## -returns



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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/97378353-8c2d-493a-8ee9-42d33ab47d18">ICreateTypeLib2</a>
 

 

