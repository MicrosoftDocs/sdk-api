---
UID: NF:wsdbase.IWSDAddress.Serialize
title: IWSDAddress::Serialize
author: windows-sdk-content
description: Assembles the component parts of the address into a string.
old-location: ncd\iwsdaddress_serialize.htm
tech.root: WsdApi
ms.assetid: 6264a2f6-39db-4c55-a0b3-2705d2093d77
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDAddress interface,Serialize method, IWSDAddress.Serialize, IWSDAddress::Serialize, Serialize, Serialize method, Serialize method,IWSDAddress interface, ncd.iwsdaddress_serialize, wsdbase/IWSDAddress::Serialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDAddress.Serialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDAddress::Serialize


## -description


Assembles the component parts of the address into a string.


## -parameters




### -param pszBuffer [out]

Buffer to receive the assembled address.


### -param cchLength [in]

Length of <i>pszBuffer</i>, in bytes.


### -param fSafe [in]

If <b>TRUE</b>, the resulting string will be network safe. For example, if you used <a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a> to build an IPv6 address, the serialized string will not contain the IPv6 scope identifier. However, if <i>fSafe</i> is <b>FALSE</b>,  then the resulting string will contain the IPv6 scope identifier. For all other <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> derived objects, there is no specific meaning for this parameter (other than ensuring that the method generate portable addresses).


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszBuffer</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The method could not be completed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a>
 

 

