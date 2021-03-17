---
UID: NF:wsdxml.WSDXMLCreateContext
title: WSDXMLCreateContext function (wsdxml.h)
description: Creates a new IWSDXMLContext object.
helpviewer_keywords: ["WSDXMLCreateContext","WSDXMLCreateContext function","ncd.wsdxmlcreatecontext","wsdxml/WSDXMLCreateContext"]
old-location: ncd\wsdxmlcreatecontext.htm
tech.root: ncd
ms.assetid: fb0d8c28-1dc3-43be-a1cf-c00de6c1f43e
ms.date: 12/05/2018
ms.keywords: WSDXMLCreateContext, WSDXMLCreateContext function, ncd.wsdxmlcreatecontext, wsdxml/WSDXMLCreateContext
req.header: wsdxml.h
req.include-header: 
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
req.lib: WsdApi.lib
req.dll: WsdApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDXMLCreateContext
 - wsdxml/WSDXMLCreateContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsdApi.dll
api_name:
 - WSDXMLCreateContext
---

# WSDXMLCreateContext function


## -description

Creates a new <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> 
    object.

## -parameters

### -param ppContext [out]

Pointer to a newly allocated 
      <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> object. If the function fails, 
      this parameter can be <b>NULL</b>.

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
<i>ppContext</i> is <b>NULL</b>.

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