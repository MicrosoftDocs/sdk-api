---
UID: NF:wsdbase.IWSDTransportAddress.GetTransportAddress
title: IWSDTransportAddress::GetTransportAddress (wsdbase.h)
description: Gets a pointer to a string representation of the address object. (IWSDTransportAddress.GetTransportAddress)
helpviewer_keywords: ["GetTransportAddress","GetTransportAddress method","GetTransportAddress method","IWSDTransportAddress interface","IWSDTransportAddress interface","GetTransportAddress method","IWSDTransportAddress.GetTransportAddress","IWSDTransportAddress::GetTransportAddress","ncd.iwsdtransportaddress_gettransportaddress","wsdbase/IWSDTransportAddress::GetTransportAddress"]
old-location: ncd\iwsdtransportaddress_gettransportaddress.htm
tech.root: ncd
ms.assetid: 090b009d-0cca-4925-bf90-cb3d0975d271
ms.date: 12/05/2018
ms.keywords: GetTransportAddress, GetTransportAddress method, GetTransportAddress method,IWSDTransportAddress interface, IWSDTransportAddress interface,GetTransportAddress method, IWSDTransportAddress.GetTransportAddress, IWSDTransportAddress::GetTransportAddress, ncd.iwsdtransportaddress_gettransportaddress, wsdbase/IWSDTransportAddress::GetTransportAddress
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
 - IWSDTransportAddress::GetTransportAddress
 - wsdbase/IWSDTransportAddress::GetTransportAddress
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
 - IWSDTransportAddress.GetTransportAddress
---

# IWSDTransportAddress::GetTransportAddress


## -description

Gets a pointer to a string representation of the address object.  The format of the string varies, and is determined by the implementing interface (either <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a> or <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>).

## -parameters

### -param ppszAddress [out]

String representation of the address object. Do not deallocate this pointer.

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
<i>ppszAddress</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The transport address has not yet been set. To set the transport address, call <a href="/windows/desktop/api/wsdbase/nf-wsdbase-iwsdtransportaddress-settransportaddress">SetTransportAddress</a> with a non-<b>NULL</b> address.

</td>
</tr>
</table>

## -remarks

The string returned by this method may contain an IPv4 or unbracketed IPv6 address such as "fe80::1".  It may also contain a bracketed IPv6 address that includes the port such as "[fe80::1]:1234".  The caller should parse the string carefully to account for both possibilities.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdtransportaddress">IWSDTransportAddress</a>
