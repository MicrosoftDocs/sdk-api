---
UID: NF:wsdbase.IWSDHttpAddress.SetSecure
title: IWSDHttpAddress::SetSecure (wsdbase.h)
description: Enables or disables TLS secure sessions for this address.
helpviewer_keywords: ["IWSDHttpAddress interface","SetSecure method","IWSDHttpAddress.SetSecure","IWSDHttpAddress::SetSecure","SetSecure","SetSecure method","SetSecure method","IWSDHttpAddress interface","ncd.iwsdhttpaddress_setsecure","wsdbase/IWSDHttpAddress::SetSecure"]
old-location: ncd\iwsdhttpaddress_setsecure.htm
tech.root: ncd
ms.assetid: f2b66d0d-51b2-437e-8ceb-a4c95f2f9d6d
ms.date: 12/05/2018
ms.keywords: IWSDHttpAddress interface,SetSecure method, IWSDHttpAddress.SetSecure, IWSDHttpAddress::SetSecure, SetSecure, SetSecure method, SetSecure method,IWSDHttpAddress interface, ncd.iwsdhttpaddress_setsecure, wsdbase/IWSDHttpAddress::SetSecure
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDHttpAddress::SetSecure
 - wsdbase/IWSDHttpAddress::SetSecure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDHttpAddress.SetSecure
---

# IWSDHttpAddress::SetSecure


## -description

Enables or disables TLS secure sessions for this address.

## -parameters

### -param fSecure [in]

<b>TRUE</b> to enable TLS secure session communications for this address, <b>FALSE</b> to disable TLS.

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

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a>