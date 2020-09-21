---
UID: NF:propsys.IPropertyDescription.GetRelativeDescriptionType
title: IPropertyDescription::GetRelativeDescriptionType (propsys.h)
description: Gets the relative description type for a property description.
old-location: properties\IPropertyDescription_GetRelativeDescriptionType.htm
tech.root: properties
ms.assetid: b3778988-63ac-4827-8098-c3c5b6b13e38
ms.date: 12/05/2018
ms.keywords: GetRelativeDescriptionType, GetRelativeDescriptionType method [Windows Properties], GetRelativeDescriptionType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetRelativeDescriptionType method, IPropertyDescription.GetRelativeDescriptionType, IPropertyDescription::GetRelativeDescriptionType, properties.IPropertyDescription_GetRelativeDescriptionType, propsys/IPropertyDescription::GetRelativeDescriptionType, shell.IPropertyDescription_GetRelativeDescriptionType, shell_IPropertyDescription_GetRelativeDescriptionType
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
 - IPropertyDescription::GetRelativeDescriptionType
 - propsys/IPropertyDescription::GetRelativeDescriptionType
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
 - IPropertyDescription.GetRelativeDescriptionType
---

# IPropertyDescription::GetRelativeDescriptionType


## -description

Gets the relative description type for a property description.

## -parameters

### -param prdt [out]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_relativedescription_type">PROPDESC_RELATIVEDESCRIPTION_TYPE</a>*</b>

When this method returns, contains a pointer to the relative description type value. See <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_relativedescription_type">PROPDESC_RELATIVEDESCRIPTION_TYPE</a> for valid values.

## -returns

Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.

## -remarks

The information retrieved by this method comes from the <i>relativeDescriptionType</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-displayinfo">displayInfo</a> element in the property's .propdesc file.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>