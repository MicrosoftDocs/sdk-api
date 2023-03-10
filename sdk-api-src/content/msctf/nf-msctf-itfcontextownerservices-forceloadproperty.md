---
UID: NF:msctf.ITfContextOwnerServices.ForceLoadProperty
title: ITfContextOwnerServices::ForceLoadProperty (msctf.h)
description: ITfContextOwnerServices::ForceLoadProperty method
helpviewer_keywords: ["ForceLoadProperty","ForceLoadProperty method [Text Services Framework]","ForceLoadProperty method [Text Services Framework]","ITfContextOwnerServices interface","ITfContextOwnerServices interface [Text Services Framework]","ForceLoadProperty method","ITfContextOwnerServices.ForceLoadProperty","ITfContextOwnerServices::ForceLoadProperty","_tsf_itfcontextownerservices_forceloadproperty_ref","msctf/ITfContextOwnerServices::ForceLoadProperty","tsf.itfcontextownerservices_forceloadproperty"]
old-location: tsf\itfcontextownerservices_forceloadproperty.htm
tech.root: TSF
ms.assetid: 7f77d82f-e048-463f-bf0d-15bf1daaddb6
ms.date: 12/05/2018
ms.keywords: ForceLoadProperty, ForceLoadProperty method [Text Services Framework], ForceLoadProperty method [Text Services Framework],ITfContextOwnerServices interface, ITfContextOwnerServices interface [Text Services Framework],ForceLoadProperty method, ITfContextOwnerServices.ForceLoadProperty, ITfContextOwnerServices::ForceLoadProperty, _tsf_itfcontextownerservices_forceloadproperty_ref, msctf/ITfContextOwnerServices::ForceLoadProperty, tsf.itfcontextownerservices_forceloadproperty
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
 - ITfContextOwnerServices::ForceLoadProperty
 - msctf/ITfContextOwnerServices::ForceLoadProperty
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
 - ITfContextOwnerServices.ForceLoadProperty
---

# ITfContextOwnerServices::ForceLoadProperty


## -description

Forces a property load.

## -parameters

### -param pProp [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a> object that specifies the property to load.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

The application must be able to grant a synchronous read-only lock before calling this method.

## -see-also

[ITfContextOwnerServices interface](nn-msctf-itfcontextownerservices.md), [ITfContextOwnerServices::Unserialize](nf-msctf-itfcontextownerservices-unserialize.md), [ITfProperty interface](nn-msctf-itfproperty.md)