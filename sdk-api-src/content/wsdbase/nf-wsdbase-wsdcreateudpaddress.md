---
UID: NF:wsdbase.WSDCreateUdpAddress
title: WSDCreateUdpAddress function (wsdbase.h)
description: Creates an IWSDUdpAddress object.
helpviewer_keywords: ["WSDCreateUdpAddress","WSDCreateUdpAddress function","ncd.wsdcreateudpaddress","wsdbase/WSDCreateUdpAddress"]
old-location: ncd\wsdcreateudpaddress.htm
tech.root: ncd
ms.assetid: 84610d5f-9b90-4830-b6d3-7b5622709668
ms.date: 12/05/2018
ms.keywords: WSDCreateUdpAddress, WSDCreateUdpAddress function, ncd.wsdcreateudpaddress, wsdbase/WSDCreateUdpAddress
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDCreateUdpAddress
 - wsdbase/WSDCreateUdpAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateUdpAddress
---

# WSDCreateUdpAddress function


## -description

Creates an <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a> object.

## -parameters

### -param ppAddress [in]

An <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a> interface pointer. This parameter cannot be <b>NULL</b>.

## -returns

This function can return one of these values.

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
<i>ppAddress</i> is <b>NULL</b>.

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