---
UID: NF:wsdbase.IWSDMessageParameters.SetRemoteAddress
title: IWSDMessageParameters::SetRemoteAddress (wsdbase.h)
description: Sets the generic address object representing the remote address to where the message is sent.
old-location: ncd\iwsdmessageparameters_setremoteaddress.htm
tech.root: WsdApi
ms.assetid: 7e762942-37b2-43ca-96e3-98594b929d98
ms.date: 12/05/2018
ms.keywords: IWSDMessageParameters interface,SetRemoteAddress method, IWSDMessageParameters.SetRemoteAddress, IWSDMessageParameters::SetRemoteAddress, SetRemoteAddress, SetRemoteAddress method, SetRemoteAddress method,IWSDMessageParameters interface, ncd.iwsdmessageparameters_setremoteaddress, wsdbase/IWSDMessageParameters::SetRemoteAddress
ms.topic: method
f1_keywords:
- wsdbase/IWSDMessageParameters.SetRemoteAddress
dev_langs:
- c++
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
- IWSDMessageParameters.SetRemoteAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDMessageParameters::SetRemoteAddress


## -description


Sets the generic address object representing the remote address to where the message is sent.


## -parameters




### -param pAddress [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a> interface that represents the remote address to where the message is sent.


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




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>
 

 

