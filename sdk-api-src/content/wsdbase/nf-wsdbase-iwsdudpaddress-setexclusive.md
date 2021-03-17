---
UID: NF:wsdbase.IWSDUdpAddress.SetExclusive
title: IWSDUdpAddress::SetExclusive (wsdbase.h)
description: Controls whether the socket is in exclusive mode.
helpviewer_keywords: ["IWSDUdpAddress interface","SetExclusive method","IWSDUdpAddress.SetExclusive","IWSDUdpAddress::SetExclusive","SetExclusive","SetExclusive method","SetExclusive method","IWSDUdpAddress interface","ncd.iwsdudpaddress_setexclusive","wsdbase/IWSDUdpAddress::SetExclusive"]
old-location: ncd\iwsdudpaddress_setexclusive.htm
tech.root: ncd
ms.assetid: 08c5ee4a-55a4-4d8b-951e-d7faed45f44f
ms.date: 12/05/2018
ms.keywords: IWSDUdpAddress interface,SetExclusive method, IWSDUdpAddress.SetExclusive, IWSDUdpAddress::SetExclusive, SetExclusive, SetExclusive method, SetExclusive method,IWSDUdpAddress interface, ncd.iwsdudpaddress_setexclusive, wsdbase/IWSDUdpAddress::SetExclusive
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
 - IWSDUdpAddress::SetExclusive
 - wsdbase/IWSDUdpAddress::SetExclusive
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
 - IWSDUdpAddress.SetExclusive
---

# IWSDUdpAddress::SetExclusive


## -description

Controls whether the socket is in exclusive mode.

## -parameters

### -param fExclusive [in]

A value of <b>TRUE</b> indicates that the socket should be set to exclusive mode. A value of <b>FALSE</b> indicates that the socket should not be in exclusive mode.

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

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>