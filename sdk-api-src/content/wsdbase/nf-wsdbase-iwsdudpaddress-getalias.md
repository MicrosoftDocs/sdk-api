---
UID: NF:wsdbase.IWSDUdpAddress.GetAlias
title: IWSDUdpAddress::GetAlias (wsdbase.h)
description: Gets the alias for the discovery address.
helpviewer_keywords: ["GetAlias","GetAlias method","GetAlias method","IWSDUdpAddress interface","IWSDUdpAddress interface","GetAlias method","IWSDUdpAddress.GetAlias","IWSDUdpAddress::GetAlias","ncd.iwsdudpaddress_getalias","wsdbase/IWSDUdpAddress::GetAlias"]
old-location: ncd\iwsdudpaddress_getalias.htm
tech.root: ncd
ms.assetid: c11a7e39-6df1-411b-9992-6ce869b0db69
ms.date: 12/05/2018
ms.keywords: GetAlias, GetAlias method, GetAlias method,IWSDUdpAddress interface, IWSDUdpAddress interface,GetAlias method, IWSDUdpAddress.GetAlias, IWSDUdpAddress::GetAlias, ncd.iwsdudpaddress_getalias, wsdbase/IWSDUdpAddress::GetAlias
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
 - IWSDUdpAddress::GetAlias
 - wsdbase/IWSDUdpAddress::GetAlias
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
 - IWSDUdpAddress.GetAlias
---

# IWSDUdpAddress::GetAlias


## -description

Gets the alias for the discovery address. This method is reserved for internal use and should not be called.

## -parameters

### -param pAlias [out]

Pointer to the alias of the discovery address.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pAlias</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>