---
UID: NF:oaidl.ICreateTypeLib2.SetCustData
title: ICreateTypeLib2::SetCustData
author: windows-sdk-content
description: Sets a value to custom data.
old-location: automat\icreatetypelib2_setcustdata.htm
tech.root: automat
ms.assetid: 7630a220-c213-4070-90e7-46ce1907127a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICreateTypeLib2 interface [Automation],SetCustData method, ICreateTypeLib2.SetCustData, ICreateTypeLib2::SetCustData, SetCustData, SetCustData method [Automation], SetCustData method [Automation],ICreateTypeLib2 interface, _oa96_ICreateTypeLib2_SetCustData, automat.icreatetypelib2_setcustdata, oaidl/ICreateTypeLib2::SetCustData
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
 - ICreateTypeLib2.SetCustData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateTypeLib2::SetCustData


## -description


Sets a value to custom data.


## -parameters




### -param guid [in]

The unique identifier for the data.




### -param pVarVal [in]

The data to store (any variant except an object).


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
 

 

