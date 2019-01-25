---
UID: NF:tapi3if.ITAddress.CreateForwardInfoObject
title: ITAddress::CreateForwardInfoObject
author: windows-sdk-content
description: The CreateForwardInfoObject method creates the forwarding information object and returns an ITForwardInformation interface pointer.
old-location: tapi3\itaddress_createforwardinfoobject.htm
tech.root: Tapi
ms.assetid: 87d37ba3-5398-47a7-808b-eb9b6681653d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateForwardInfoObject, CreateForwardInfoObject method [TAPI 2.2], CreateForwardInfoObject method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],CreateForwardInfoObject method, ITAddress.CreateForwardInfoObject, ITAddress::CreateForwardInfoObject, _tapi3_itaddress_createforwardinfoobject, tapi3.itaddress_createforwardinfoobject, tapi3if/ITAddress::CreateForwardInfoObject
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress.CreateForwardInfoObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress::CreateForwardInfoObject


## -description


The 
<b>CreateForwardInfoObject</b> method creates the forwarding information object and returns an 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> interface pointer. This interface exposes methods that allow an application to control aspects of how a call is forwarded, such as whether internal calls will be handled differently than external calls.


## -parameters




### -param ppForwardInfo [out]

Pointer to 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppForwardInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must set information on a newly created 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> object before the object can be used.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> interface returned by <b>ITAddress::CreateForwardInfoObject</b>. The application must call <b>Release</b> on the 
<b>ITForwardInformation</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">Forward</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">get_CurrentForwardInfo</a>
 

 

