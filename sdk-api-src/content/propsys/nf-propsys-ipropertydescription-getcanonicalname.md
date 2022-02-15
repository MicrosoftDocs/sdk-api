---
UID: NF:propsys.IPropertyDescription.GetCanonicalName
title: IPropertyDescription::GetCanonicalName (propsys.h)
description: Gets the case-sensitive name by which a property is known to the system, regardless of its localized name.
old-location: properties\IPropertyDescription_GetCanonicalName.htm
tech.root: properties
ms.assetid: 861c3b48-77cf-4f72-b85f-a6f921571dd7
ms.date: 12/05/2018
ms.keywords: GetCanonicalName, GetCanonicalName method [Windows Properties], GetCanonicalName method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetCanonicalName method, IPropertyDescription.GetCanonicalName, IPropertyDescription::GetCanonicalName, properties.IPropertyDescription_GetCanonicalName, propsys/IPropertyDescription::GetCanonicalName, shell.IPropertyDescription_GetCanonicalName, shell_IPropertyDescription_GetCanonicalName
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescription::GetCanonicalName
 - propsys/IPropertyDescription::GetCanonicalName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.GetCanonicalName
---

# IPropertyDescription::GetCanonicalName


## -description

Gets the case-sensitive name by which a property is known to the system, regardless of its localized name.

## -parameters

### -param ppszName [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the property's canonical name as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The information retrieved by this method comes from the <i>name</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-propertydescription">propertyDescription</a> element in the property's .propdesc file.

It is the responsibility of the calling application to use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the string referred to by <i>ppszName</i> when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>