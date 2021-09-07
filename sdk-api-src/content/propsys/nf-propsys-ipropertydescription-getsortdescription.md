---
UID: NF:propsys.IPropertyDescription.GetSortDescription
title: IPropertyDescription::GetSortDescription (propsys.h)
description: Gets the current sort description flags for the property, which indicate the particular wordings of sort offerings.
old-location: properties\IPropertyDescription_GetSortDescription.htm
tech.root: properties
ms.assetid: 71f565b3-cf77-498c-b2a5-3a49a71c102f
ms.date: 12/05/2018
ms.keywords: GetSortDescription, GetSortDescription method [Windows Properties], GetSortDescription method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetSortDescription method, IPropertyDescription.GetSortDescription, IPropertyDescription::GetSortDescription, PDSD_A_Z, PDSD_GENERAL, PDSD_LOWEST_HIGHEST, PDSD_OLDEST_NEWEST, PDSD_SMALLEST_BIGGEST, properties.IPropertyDescription_GetSortDescription, propsys/IPropertyDescription::GetSortDescription, shell.IPropertyDescription_GetSortDescription, shell_IPropertyDescription_GetSortDescription
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
 - IPropertyDescription::GetSortDescription
 - propsys/IPropertyDescription::GetSortDescription
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
 - IPropertyDescription.GetSortDescription
---

# IPropertyDescription::GetSortDescription


## -description

Gets the current sort description flags for the property, which indicate the particular wordings of sort offerings.

## -parameters

### -param psd [out]

Type: <b>PROPDESC_SORTDESCRIPTION*</b>

When this method returns, contains a pointer to the value of one or more of the following flags that indicate the sort types available to the user. Note that the strings shown are English versions only. Localized strings are used for other locales.



#### PDSD_GENERAL

Default. "Sort going up", "Sort going down"



#### PDSD_A_Z

"A on top", "Z on top"



#### PDSD_LOWEST_HIGHEST

"Lowest on top", "Highest on top"



#### PDSD_SMALLEST_BIGGEST

"Smallest on top", "Largest on top"



#### PDSD_OLDEST_NEWEST

"Oldest on top", "Newest on top"

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The settings retrieved by this method are set through the <i>sortDescription</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-labelinfo">labelInfo</a> element in the property's .propdesc file.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>