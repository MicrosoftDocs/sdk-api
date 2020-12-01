---
UID: NF:msctf.ITextStoreACPServices.ForceLoadProperty
title: ITextStoreACPServices::ForceLoadProperty (msctf.h)
description: ITextStoreACPServices::ForceLoadProperty method
helpviewer_keywords: ["ForceLoadProperty","ForceLoadProperty method [Text Services Framework]","ForceLoadProperty method [Text Services Framework]","ITextStoreACPServices interface","ITextStoreACPServices interface [Text Services Framework]","ForceLoadProperty method","ITextStoreACPServices.ForceLoadProperty","ITextStoreACPServices::ForceLoadProperty","_tsf_itextstoreacpservices_forceloadproperty_ref","msctf/ITextStoreACPServices::ForceLoadProperty","tsf.itextstoreacpservices_forceloadproperty"]
old-location: tsf\itextstoreacpservices_forceloadproperty.htm
tech.root: TSF
ms.assetid: 6792ccc0-7bbd-479c-9f24-a283ce03c7fe
ms.date: 12/05/2018
ms.keywords: ForceLoadProperty, ForceLoadProperty method [Text Services Framework], ForceLoadProperty method [Text Services Framework],ITextStoreACPServices interface, ITextStoreACPServices interface [Text Services Framework],ForceLoadProperty method, ITextStoreACPServices.ForceLoadProperty, ITextStoreACPServices::ForceLoadProperty, _tsf_itextstoreacpservices_forceloadproperty_ref, msctf/ITextStoreACPServices::ForceLoadProperty, tsf.itextstoreacpservices_forceloadproperty
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
 - ITextStoreACPServices::ForceLoadProperty
 - msctf/ITextStoreACPServices::ForceLoadProperty
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
 - ITextStoreACPServices.ForceLoadProperty
---

# ITextStoreACPServices::ForceLoadProperty


## -description

Forces all values of an asynchronously loaded property to be loaded.

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

When calling this method, the application must be able to grant a synchronous read-only lock.

## -see-also

[ITextStoreACPServices interface](nn-msctf-itextstoreacpservices.md), [ITextStoreACPServices::Unserialize](nf-msctf-itextstoreacpservices-unserialize.md), [ITfPersistentPropertyLoaderACP interface](nn-msctf-itfpersistentpropertyloaderacp.md), [ITfProperty interface](nn-msctf-itfproperty.md)