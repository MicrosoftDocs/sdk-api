---
UID: NF:propsys.IPropertyDescription.GetTypeFlags
title: IPropertyDescription::GetTypeFlags (propsys.h)
description: Gets a set of flags that describe the uses and capabilities of the property.
old-location: properties\IPropertyDescription_GetTypeFlags.htm
tech.root: properties
ms.assetid: 20ff02c1-72de-479f-afd8-29ec580bbfcb
ms.date: 12/05/2018
ms.keywords: GetTypeFlags, GetTypeFlags method [Windows Properties], GetTypeFlags method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetTypeFlags method, IPropertyDescription.GetTypeFlags, IPropertyDescription::GetTypeFlags, properties.IPropertyDescription_GetTypeFlags, propsys/IPropertyDescription::GetTypeFlags, shell.IPropertyDescription_GetTypeFlags, shell_IPropertyDescription_GetTypeFlags
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
 - IPropertyDescription::GetTypeFlags
 - propsys/IPropertyDescription::GetTypeFlags
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
 - IPropertyDescription.GetTypeFlags
---

# IPropertyDescription::GetTypeFlags


## -description

Gets a set of flags that describe the uses and capabilities of the property.

## -parameters

### -param mask [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_type_flags">PROPDESC_TYPE_FLAGS</a></b>

A mask that specifies which type flags to retrieve. A combination of values found in the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_type_flags">PROPDESC_TYPE_FLAGS</a> constants. To retrieve all type flags, pass <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_type_flags">PDTF_MASK_ALL</a>

### -param ppdtFlags [out]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_type_flags">PROPDESC_TYPE_FLAGS</a>*</b>

When this method returns, contains a pointer to a value that consists of bitwise <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_type_flags">PROPDESC_TYPE_FLAGS</a> values.

## -returns

Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.

## -remarks

If the property description instance comes from <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescription">PSGetPropertyDescription</a> or <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionbyname">PSGetPropertyDescriptionByName</a>, these flags come from the .propdesc file that defines the property description.

If the instance comes from <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcolorprofileresourcecollection-getat">GetAt</a>, the type flags come from the .propdesc file and may be influenced by the specific proplist. This means that flags obtained from one property description instance may be slightly different from another instance (both referring to the same property).

For additional information on type flags, see the <i>canGroupBy</i>, <i>canStackBy</i>, <i>isInnate</i>, <i>multipleValues</i>, <i>isGroup</i>, <i>isTreeProperty</i>, <i>isViewable</i>, <i>isQueryable</i>, and <i>includeInFullTextQuery</i> attributes of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>