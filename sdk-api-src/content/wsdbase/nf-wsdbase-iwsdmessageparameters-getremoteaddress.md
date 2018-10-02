---
UID: NF:wsdbase.IWSDMessageParameters.GetRemoteAddress
title: IWSDMessageParameters::GetRemoteAddress
author: windows-sdk-content
description: Retrieves the generic address object representing the remote address from which the message was sent.
old-location: ncd\iwsdmessageparameters_getremoteaddress.htm
tech.root: WsdApi
ms.assetid: 483306d4-9672-4f30-a318-df5c7afbf583
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRemoteAddress, GetRemoteAddress method, GetRemoteAddress method,IWSDMessageParameters interface, IWSDMessageParameters interface,GetRemoteAddress method, IWSDMessageParameters.GetRemoteAddress, IWSDMessageParameters::GetRemoteAddress, ncd.iwsdmessageparameters_getremoteaddress, wsdbase/IWSDMessageParameters::GetRemoteAddress
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
 - IWSDMessageParameters.GetRemoteAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDMessageParameters::GetRemoteAddress


## -description


Retrieves the generic address object representing the remote address from which the message was sent.


## -parameters




### -param ppAddress [out]

An <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> interface that represents the remote address from which the message was sent.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
<i>ppAddress</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The caller is responsible for releasing memory allocated to <i>ppAddress</i>.




## -see-also




<a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>
 

 

