---
UID: NF:wsdbase.IWSDTransportAddress.GetTransportAddressEx
title: IWSDTransportAddress::GetTransportAddressEx (wsdbase.h)
description: Gets a pointer to a string representation of the address object. (IWSDTransportAddress.GetTransportAddressEx)
helpviewer_keywords: ["GetTransportAddressEx","GetTransportAddressEx method","GetTransportAddressEx method","IWSDTransportAddress interface","IWSDTransportAddress interface","GetTransportAddressEx method","IWSDTransportAddress.GetTransportAddressEx","IWSDTransportAddress::GetTransportAddressEx","ncd.iwsdtransportaddress_gettransportaddressex","wsdbase/IWSDTransportAddress::GetTransportAddressEx"]
old-location: ncd\iwsdtransportaddress_gettransportaddressex.htm
tech.root: ncd
ms.assetid: 4b6f8e97-6387-4f2b-8388-775cc84e92f0
ms.date: 12/05/2018
ms.keywords: GetTransportAddressEx, GetTransportAddressEx method, GetTransportAddressEx method,IWSDTransportAddress interface, IWSDTransportAddress interface,GetTransportAddressEx method, IWSDTransportAddress.GetTransportAddressEx, IWSDTransportAddress::GetTransportAddressEx, ncd.iwsdtransportaddress_gettransportaddressex, wsdbase/IWSDTransportAddress::GetTransportAddressEx
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
 - IWSDTransportAddress::GetTransportAddressEx
 - wsdbase/IWSDTransportAddress::GetTransportAddressEx
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
 - IWSDTransportAddress.GetTransportAddressEx
---

# IWSDTransportAddress::GetTransportAddressEx


## -description

Gets a pointer to a string representation of the address object.  The format of the string varies, and is determined by the implementing interface (either <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a> or <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>).

## -parameters

### -param fSafe [in]

Specifies whether the scope identifier for an IPv6 address is included in the returned <i>ppszAddress</i> string. For example, if the address object represents an IPv6 link local address and <i>fSafe</i> is <b>FALSE</b>, then the IPv6 scope identifier will be included in the returned <i>ppszAddress</i> string.

If the address object represents an IPv4 address or a host name, this parameter is ignored.

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
