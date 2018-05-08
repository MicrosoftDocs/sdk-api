---
UID: NF:oaidl.ICreateTypeInfo.SetGuid
title: ICreateTypeInfo::SetGuid
author: windows-driver-content
description: Sets the globally unique identifier (GUID) associated with the type description.
old-location: automat\icreatetypeinfo_setguid.htm
old-project: automat
ms.assetid: 031bc83d-8e0c-49da-aa15-cd44af469592
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetGuid method, ICreateTypeInfo.SetGuid, ICreateTypeInfo::SetGuid, SetGuid, SetGuid method [Automation], SetGuid method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetGuid, automat.icreatetypeinfo_setguid, oaidl/ICreateTypeInfo::SetGuid
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
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	ICreateTypeInfo.SetGuid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ICreateTypeInfo::SetGuid


## -description


Sets the globally unique identifier (GUID) associated with the type description.


## -parameters




### -param guid [in]

The globally unique ID to be associated with the type description.



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
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot write to the destination.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



For an interface, this is an interface ID (IID); for a coclass, it is a class ID (CLSID). For information on GUIDs, see <a href="https://msdn.microsoft.com/c4061d23-b6bd-43f4-adf0-5980dae7a059">Type Libraries and the Object Description Language</a>.




## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

