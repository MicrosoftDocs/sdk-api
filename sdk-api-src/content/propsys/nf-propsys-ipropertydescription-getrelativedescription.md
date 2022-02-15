---
UID: NF:propsys.IPropertyDescription.GetRelativeDescription
title: IPropertyDescription::GetRelativeDescription (propsys.h)
description: Compares two property values in the manner specified by the property description. Returns two display strings that describe how the two properties compare.
old-location: properties\IPropertyDescription_GetRelativeDescription.htm
tech.root: properties
ms.assetid: d98cc2de-8f1c-4827-99b9-2b770d1270e3
ms.date: 12/05/2018
ms.keywords: GetRelativeDescription, GetRelativeDescription method [Windows Properties], GetRelativeDescription method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetRelativeDescription method, IPropertyDescription.GetRelativeDescription, IPropertyDescription::GetRelativeDescription, properties.IPropertyDescription_GetRelativeDescription, propsys/IPropertyDescription::GetRelativeDescription, shell.IPropertyDescription_GetRelativeDescription, shell_IPropertyDescription_GetRelativeDescription
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
 - IPropertyDescription::GetRelativeDescription
 - propsys/IPropertyDescription::GetRelativeDescription
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
 - IPropertyDescription.GetRelativeDescription
---

# IPropertyDescription::GetRelativeDescription


## -description

Compares two property values in the manner specified by the property description. Returns two display strings that describe how the two properties compare.

## -parameters

### -param propvar1 [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the type and value of the first property.

### -param propvar2 [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the type and value of the second property.

### -param ppszDesc1 [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the description string that compares the first property with the second property. The string is null-terminated.

### -param ppszDesc2 [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the description string that compares the second property with the first property. The string is null-terminated.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is influenced by the <i>relativeDescriptionType</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-displayinfo">displayInfo</a> element in the property's .propdesc file.

It is the responsibility of the calling application to release <i>ppszDesc1</i> and <i>ppszDesc2</i> through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when they are no longer needed.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>