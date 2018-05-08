---
UID: NF:wsdbase.IWSDMessageParameters.SetRemoteAddress
title: IWSDMessageParameters::SetRemoteAddress
author: windows-driver-content
description: Sets the generic address object representing the remote address to where the message is sent.
old-location: ncd\iwsdmessageparameters_setremoteaddress.htm
old-project: WsdApi
ms.assetid: 7e762942-37b2-43ca-96e3-98594b929d98
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDMessageParameters interface,SetRemoteAddress method, IWSDMessageParameters.SetRemoteAddress, IWSDMessageParameters::SetRemoteAddress, SetRemoteAddress, SetRemoteAddress method, SetRemoteAddress method,IWSDMessageParameters interface, ncd.iwsdmessageparameters_setremoteaddress, wsdbase/IWSDMessageParameters::SetRemoteAddress
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
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wsdapi.dll
api_name:
-	IWSDMessageParameters.SetRemoteAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDMessageParameters::SetRemoteAddress


## -description


Sets the generic address object representing the remote address to where the message is sent.


## -parameters




### -param pAddress [in]

An <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> interface that represents the remote address to where the message is sent.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>
 

 

