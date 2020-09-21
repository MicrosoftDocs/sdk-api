---
UID: NF:wsdbase.IWSDTransportAddress.GetPort
title: IWSDTransportAddress::GetPort (wsdbase.h)
description: Gets the IP port number associated with this transport address.
helpviewer_keywords: ["GetPort","GetPort method","GetPort method","IWSDTransportAddress interface","IWSDTransportAddress interface","GetPort method","IWSDTransportAddress.GetPort","IWSDTransportAddress::GetPort","ncd.iwsdtransportaddress_getport","wsdbase/IWSDTransportAddress::GetPort"]
old-location: ncd\iwsdtransportaddress_getport.htm
tech.root: ncd
ms.assetid: cc2e623f-e6b6-42ad-b0de-7960de0142d0
ms.date: 12/05/2018
ms.keywords: GetPort, GetPort method, GetPort method,IWSDTransportAddress interface, IWSDTransportAddress interface,GetPort method, IWSDTransportAddress.GetPort, IWSDTransportAddress::GetPort, ncd.iwsdtransportaddress_getport, wsdbase/IWSDTransportAddress::GetPort
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
 - IWSDTransportAddress::GetPort
 - wsdbase/IWSDTransportAddress::GetPort
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
 - IWSDTransportAddress.GetPort
---

# IWSDTransportAddress::GetPort


## -description

Gets the IP port number associated with this transport address.

## -parameters

### -param pwPort [out]

Port number associated with the address object.

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
<i>pwPort</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdtransportaddress">IWSDTransportAddress</a>