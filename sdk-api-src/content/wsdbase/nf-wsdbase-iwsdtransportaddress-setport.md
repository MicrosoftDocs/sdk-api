---
UID: NF:wsdbase.IWSDTransportAddress.SetPort
title: IWSDTransportAddress::SetPort (wsdbase.h)
description: Sets only the IP port number for this transport address.
helpviewer_keywords: ["IWSDTransportAddress interface","SetPort method","IWSDTransportAddress.SetPort","IWSDTransportAddress::SetPort","SetPort","SetPort method","SetPort method","IWSDTransportAddress interface","ncd.iwsdtransportaddress_setport","wsdbase/IWSDTransportAddress::SetPort"]
old-location: ncd\iwsdtransportaddress_setport.htm
tech.root: ncd
ms.assetid: 0959e6f9-82cf-4634-9547-682df1965efa
ms.date: 12/05/2018
ms.keywords: IWSDTransportAddress interface,SetPort method, IWSDTransportAddress.SetPort, IWSDTransportAddress::SetPort, SetPort, SetPort method, SetPort method,IWSDTransportAddress interface, ncd.iwsdtransportaddress_setport, wsdbase/IWSDTransportAddress::SetPort
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
 - IWSDTransportAddress::SetPort
 - wsdbase/IWSDTransportAddress::SetPort
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
 - IWSDTransportAddress.SetPort
---

# IWSDTransportAddress::SetPort


## -description

Sets only the IP port number for this transport address.

## -parameters

### -param wPort [in]

The IP port number for the address object.

## -returns

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
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdtransportaddress">IWSDTransportAddress</a>