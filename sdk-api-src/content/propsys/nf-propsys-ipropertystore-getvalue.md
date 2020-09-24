---
UID: NF:propsys.IPropertyStore.GetValue
title: IPropertyStore::GetValue (propsys.h)
description: This method retrieves the data for a specific property.
helpviewer_keywords: ["GetValue","GetValue (IPropertyStore)","GetValue method [Audio Devices]","GetValue method [Audio Devices]","IPropertyStore interface","IPropertyStore interface [Audio Devices]","GetValue method","IPropertyStore.GetValue","IPropertyStore::GetValue","audio.ipropertystore_getvalue","audio_syseffects_r_5540088b-f979-440e-93b8-feb9db17001c.xml","propsys/IPropertyStore::GetValue"]
old-location: audio\ipropertystore_getvalue.htm
tech.root: audio
ms.assetid: 11204335-0f00-4af8-8787-93e91248e5bd
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue (IPropertyStore), GetValue method [Audio Devices], GetValue method [Audio Devices],IPropertyStore interface, IPropertyStore interface [Audio Devices],GetValue method, IPropertyStore.GetValue, IPropertyStore::GetValue, audio.ipropertystore_getvalue, audio_syseffects_r_5540088b-f979-440e-93b8-feb9db17001c.xml, propsys/IPropertyStore::GetValue
req.header: propsys.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later versions of the Windows operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.idl
req.dll: 
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyStore::GetValue
 - propsys/IPropertyStore::GetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.idl
 - Propsys.idl.dll
api_name:
 - IPropertyStore.GetValue
---

# IPropertyStore::GetValue


## -description

This method retrieves the data for a specific property.

## -parameters

### -param key

TBD

### -param pv

After the <code>IPropertyStore::GetValue</code> method returns successfully, this parameter points to a <a href="/previous-versions/aa912007(v=msdn.10)">PROPVARIANT </a> structure that contains data about the property.

### -param Key

A reference to the PROPERTYKEY structure that is retrieved through <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a>. The PROPERTYKEY structure also contains a globally unique identifier (GUID) for the property.

## -returns

Returns S_OK or INPLACE_S_TRUNCATED if successful, or an error value otherwise. 

INPLACE_S_TRUNCATED is returned to indicate that the returned PROPVARIANT was converted into a more canonical form. For example, this would be done to trim leading or trailing spaces from a string value. You must use the SUCCEEDED macro to check the return value, which treats INPLACE_S_TRUNCATED as a success code. The SUCCEEDED macro is defined in the Winerror.h file.

## -remarks

If the PROPERTYKEY referenced in key is not present in the property store, this method returns S_OK and the <a href="/previous-versions/aa912007(v=msdn.10)">vt </a> member of the structure that is pointed to by pv is set to VT_EMPTY.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a>