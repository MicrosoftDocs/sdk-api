---
UID: NF:wsdbase.IWSDHttpAddress.GetSecure
title: IWSDHttpAddress::GetSecure (wsdbase.h)
description: Retrieves the status on whether TLS secure sessions are enabled for this address.
helpviewer_keywords: ["GetSecure","GetSecure method","GetSecure method","IWSDHttpAddress interface","IWSDHttpAddress interface","GetSecure method","IWSDHttpAddress.GetSecure","IWSDHttpAddress::GetSecure","ncd.iwsdhttpaddress_getsecure","wsdbase/IWSDHttpAddress::GetSecure"]
old-location: ncd\iwsdhttpaddress_getsecure.htm
tech.root: ncd
ms.assetid: aaf9e918-7d1c-4457-94f8-888a99f07c18
ms.date: 12/05/2018
ms.keywords: GetSecure, GetSecure method, GetSecure method,IWSDHttpAddress interface, IWSDHttpAddress interface,GetSecure method, IWSDHttpAddress.GetSecure, IWSDHttpAddress::GetSecure, ncd.iwsdhttpaddress_getsecure, wsdbase/IWSDHttpAddress::GetSecure
f1_keywords:
- wsdbase/IWSDHttpAddress.GetSecure
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
- Wsdapi.dll
api_name:
- IWSDHttpAddress.GetSecure
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDHttpAddress::GetSecure


## -description


Retrieves the status on whether TLS secure sessions are enabled for this address.


## -parameters






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
TLS secure sessions are enabled for this address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
TLS secure sessions are disabled for this address.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a>
 

 

