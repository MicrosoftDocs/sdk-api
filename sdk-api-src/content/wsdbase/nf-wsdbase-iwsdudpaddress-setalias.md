---
UID: NF:wsdbase.IWSDUdpAddress.SetAlias
title: IWSDUdpAddress::SetAlias (wsdbase.h)
description: Sets the alias for the discovery address.
helpviewer_keywords: ["IWSDUdpAddress interface","SetAlias method","IWSDUdpAddress.SetAlias","IWSDUdpAddress::SetAlias","SetAlias","SetAlias method","SetAlias method","IWSDUdpAddress interface","ncd.iwsdudpaddress_setalias","wsdbase/IWSDUdpAddress::SetAlias"]
old-location: ncd\iwsdudpaddress_setalias.htm
tech.root: ncd
ms.assetid: 2156f271-cad4-4160-8d1f-bc44dc7b0e9f
ms.date: 12/05/2018
ms.keywords: IWSDUdpAddress interface,SetAlias method, IWSDUdpAddress.SetAlias, IWSDUdpAddress::SetAlias, SetAlias, SetAlias method, SetAlias method,IWSDUdpAddress interface, ncd.iwsdudpaddress_setalias, wsdbase/IWSDUdpAddress::SetAlias
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
 - IWSDUdpAddress::SetAlias
 - wsdbase/IWSDUdpAddress::SetAlias
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
 - IWSDUdpAddress.SetAlias
---

# IWSDUdpAddress::SetAlias


## -description

Sets the alias for the discovery address. This method is reserved for internal use and should not be called.

## -parameters

### -param pAlias [in]

A pointer to the alias of the discovery address.

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