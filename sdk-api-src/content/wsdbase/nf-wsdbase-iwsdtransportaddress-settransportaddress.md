---
UID: NF:wsdbase.IWSDTransportAddress.SetTransportAddress
title: IWSDTransportAddress::SetTransportAddress (wsdbase.h)
description: Sets the string representation of the transport address.
helpviewer_keywords: ["IWSDTransportAddress interface","SetTransportAddress method","IWSDTransportAddress.SetTransportAddress","IWSDTransportAddress::SetTransportAddress","SetTransportAddress","SetTransportAddress method","SetTransportAddress method","IWSDTransportAddress interface","ncd.iwsdtransportaddress_settransportaddress","wsdbase/IWSDTransportAddress::SetTransportAddress"]
old-location: ncd\iwsdtransportaddress_settransportaddress.htm
tech.root: ncd
ms.assetid: ea87b7d8-71c0-4cb6-b28b-7ac8f2417886
ms.date: 12/05/2018
ms.keywords: IWSDTransportAddress interface,SetTransportAddress method, IWSDTransportAddress.SetTransportAddress, IWSDTransportAddress::SetTransportAddress, SetTransportAddress, SetTransportAddress method, SetTransportAddress method,IWSDTransportAddress interface, ncd.iwsdtransportaddress_settransportaddress, wsdbase/IWSDTransportAddress::SetTransportAddress
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
 - IWSDTransportAddress::SetTransportAddress
 - wsdbase/IWSDTransportAddress::SetTransportAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDTransportAddress.SetTransportAddress
---

# IWSDTransportAddress::SetTransportAddress


## -description

Sets the string representation of the transport address.  The format of the string varies, and is determined by the implementing interface (either <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a> or <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>).

## -parameters

### -param pszAddress [in]

String representation of the transport address.

## -returns

This method can return one of these values.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of the address string pointed to by <i>ppszAddress</i> exceeds WSD_MAX_TEXT_LENGTH (8192),  <i>ppszAddress</i> is <b>NULL</b>, or the format of <i>ppszAddress</i> was not recognized. 

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
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdtransportaddress">IWSDTransportAddress</a>