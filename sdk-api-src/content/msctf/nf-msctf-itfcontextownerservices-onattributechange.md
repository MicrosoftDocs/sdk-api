---
UID: NF:msctf.ITfContextOwnerServices.OnAttributeChange
title: ITfContextOwnerServices::OnAttributeChange (msctf.h)
description: ITfContextOwnerServices::OnAttributeChange method
helpviewer_keywords: ["ITfContextOwnerServices interface [Text Services Framework]","OnAttributeChange method","ITfContextOwnerServices.OnAttributeChange","ITfContextOwnerServices::OnAttributeChange","OnAttributeChange","OnAttributeChange method [Text Services Framework]","OnAttributeChange method [Text Services Framework]","ITfContextOwnerServices interface","_tsf_itfcontextownerservices_onattributechange_ref","msctf/ITfContextOwnerServices::OnAttributeChange","tsf.itfcontextownerservices_onattributechange"]
old-location: tsf\itfcontextownerservices_onattributechange.htm
tech.root: TSF
ms.assetid: 8aae92e2-ae08-4e87-88f1-ece448323866
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],OnAttributeChange method, ITfContextOwnerServices.OnAttributeChange, ITfContextOwnerServices::OnAttributeChange, OnAttributeChange, OnAttributeChange method [Text Services Framework], OnAttributeChange method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_onattributechange_ref, msctf/ITfContextOwnerServices::OnAttributeChange, tsf.itfcontextownerservices_onattributechange
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwnerServices::OnAttributeChange
 - msctf/ITfContextOwnerServices::OnAttributeChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerServices.OnAttributeChange
---

# ITfContextOwnerServices::OnAttributeChange


## -description

Called by a context owner to generate notifications that a support attribute value changed.

## -parameters

### -param rguidAttribute [in]

Specifies the GUID of the support attribute.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

A support attribute is a read-only property maintained by the context owner. The supported attributes are in the Tsattrs.h header file.

## -see-also

[ITfContextOwnerServices interface](nn-msctf-itfcontextownerservices.md)

