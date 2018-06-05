---
UID: NF:oaidl.ICreateTypeLib.SaveAllChanges
title: ICreateTypeLib::SaveAllChanges
author: windows-sdk-content
description: Saves the ICreateTypeLib instance following the layout of type information.
old-location: automat\icreatetypelib_saveallchanges.htm
old-project: automat
ms.assetid: 67824f38-e515-487e-8f4b-6682a5ac669c
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: ICreateTypeLib interface [Automation],SaveAllChanges method, ICreateTypeLib.SaveAllChanges, ICreateTypeLib::SaveAllChanges, SaveAllChanges, SaveAllChanges method [Automation], SaveAllChanges method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SaveAllChanges, automat.icreatetypelib_saveallchanges, oaidl/ICreateTypeLib::SaveAllChanges
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	ICreateTypeLib.SaveAllChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ICreateTypeLib::SaveAllChanges


## -description


Saves the <a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a> instance following the layout of type information.


## -parameters






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
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_IOERROR</b></dt>
</dl>
</td>
<td width="60%">
The function cannot write to the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.

</td>
</tr>
</table>
 




## -remarks



You should not call any other <a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a> methods after calling <b>SaveAllChanges</b>.





## -see-also




<a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a>
 

 

