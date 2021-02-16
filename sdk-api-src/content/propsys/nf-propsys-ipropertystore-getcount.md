---
UID: NF:propsys.IPropertyStore.GetCount
title: IPropertyStore::GetCount (propsys.h)
description: This method returns a count of the number of properties that are attached to the file.
helpviewer_keywords: ["GetCount","GetCount (IPropertyStore)","GetCount method [Audio Devices]","GetCount method [Audio Devices]","IPropertyStore interface","IPropertyStore interface [Audio Devices]","GetCount method","IPropertyStore.GetCount","IPropertyStore::GetCount","audio.ipropertystore_getcount","audio_syseffects_r_2670eef9-2f2a-4e3d-8a43-d8d61a9ebce5.xml","propsys/IPropertyStore::GetCount"]
old-location: audio\ipropertystore_getcount.htm
tech.root: audio
ms.assetid: 23f7b982-29db-4960-9a1d-2f9e033ebf61
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount (IPropertyStore), GetCount method [Audio Devices], GetCount method [Audio Devices],IPropertyStore interface, IPropertyStore interface [Audio Devices],GetCount method, IPropertyStore.GetCount, IPropertyStore::GetCount, audio.ipropertystore_getcount, audio_syseffects_r_2670eef9-2f2a-4e3d-8a43-d8d61a9ebce5.xml, propsys/IPropertyStore::GetCount
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
 - IPropertyStore::GetCount
 - propsys/IPropertyStore::GetCount
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
 - IPropertyStore.GetCount
---

# IPropertyStore::GetCount


## -description

This method returns a count of the number of properties that are attached to the file.

## -parameters

### -param cProps

A pointer to a value that indicates the property count.

## -returns

The <code>IpropertyStore::GetCount</code> method returns a value of S_OK when the call is successful, even if the file has no properties attached. Any other code returned is an error code.

## -remarks

<b>IPropertyStore</b> provides an abstraction over an array of property keys via the <code>IPropertyStore::GetCount</code> and <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a> methods. The property keys in this array represent the properties that are currently stored by the <b>IPropertyStore</b>.

When <code>GetCount</code> succeeds, the value pointed to by cProps is a count of property keys in the array. The caller can expect calls to <b>IPropertyStore::GetAt</b> to succeed for values of iProp less than cProps.

In the case of failures such as E_OUTOFMEMORY, you should set cProps to zero. It is preferable that errors are discovered during creation or initialization of the property store.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a>