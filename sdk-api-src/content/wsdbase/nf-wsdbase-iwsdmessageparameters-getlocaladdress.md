---
UID: NF:wsdbase.IWSDMessageParameters.GetLocalAddress
title: IWSDMessageParameters::GetLocalAddress
author: windows-sdk-content
description: Retrieves the generic address object representing the local address that received the message.
old-location: ncd\iwsdmessageparameters_getlocaladdress.htm
old-project: WsdApi
ms.assetid: 97eab68f-9a77-46ae-a50e-be6267e25040
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetLocalAddress, GetLocalAddress method, GetLocalAddress method,IWSDMessageParameters interface, IWSDMessageParameters interface,GetLocalAddress method, IWSDMessageParameters.GetLocalAddress, IWSDMessageParameters::GetLocalAddress, ncd.iwsdmessageparameters_getlocaladdress, wsdbase/IWSDMessageParameters::GetLocalAddress
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDMessageParameters.GetLocalAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDMessageParameters::GetLocalAddress


## -description


Retrieves the generic address object representing the local address that received the message.


## -parameters




### -param ppAddress [out]

An <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> interface that represents the local address that received the message.


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
 

 

