---
UID: NF:propsys.IPropertyDescription.GetSortDescriptionLabel
title: IPropertyDescription::GetSortDescriptionLabel (propsys.h)
description: Gets the localized display string that describes the current sort order.
old-location: properties\IPropertyDescription_GetSortDescriptionLabel.htm
tech.root: properties
ms.assetid: 5cfa445b-953b-474f-ba7b-1ed6cfbf981d
ms.date: 12/05/2018
ms.keywords: GetSortDescriptionLabel, GetSortDescriptionLabel method [Windows Properties], GetSortDescriptionLabel method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetSortDescriptionLabel method, IPropertyDescription.GetSortDescriptionLabel, IPropertyDescription::GetSortDescriptionLabel, properties.IPropertyDescription_GetSortDescriptionLabel, propsys/IPropertyDescription::GetSortDescriptionLabel, shell.IPropertyDescription_GetSortDescriptionLabel, shell_IPropertyDescription_GetSortDescriptionLabel
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
 - IPropertyDescription::GetSortDescriptionLabel
 - propsys/IPropertyDescription::GetSortDescriptionLabel
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
 - IPropertyDescription.GetSortDescriptionLabel
---

# IPropertyDescription::GetSortDescriptionLabel


## -description

Gets the localized display string that describes the current sort order.

## -parameters

### -param fDescending [in]

Type: <b>BOOL*</b>

<b>TRUE</b> if <i>ppszDescription</i> should reference the string "Z on top"; <b>FALSE</b> to reference the string "A on top".

### -param ppszDescription [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the sort description as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The string retrieved by this method is determined by flags set in the <i>sortDescription</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-labelinfo">labelInfo</a> element in the property's .propdesc file.

It is the responsibility of the calling application to release <i>ppszDescription</i> when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>