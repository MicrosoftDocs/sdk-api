---
UID: NF:propsys.IPropertyDescription.GetSortDescription
title: IPropertyDescription::GetSortDescription (propsys.h)
author: windows-sdk-content
description: Gets the current sort description flags for the property, which indicate the particular wordings of sort offerings.
old-location: properties\IPropertyDescription_GetSortDescription.htm
tech.root: properties
ms.assetid: 71f565b3-cf77-498c-b2a5-3a49a71c102f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSortDescription, GetSortDescription method [Windows Properties], GetSortDescription method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetSortDescription method, IPropertyDescription.GetSortDescription, IPropertyDescription::GetSortDescription, PDSD_A_Z, PDSD_GENERAL, PDSD_LOWEST_HIGHEST, PDSD_OLDEST_NEWEST, PDSD_SMALLEST_BIGGEST, properties.IPropertyDescription_GetSortDescription, propsys/IPropertyDescription::GetSortDescription, shell.IPropertyDescription_GetSortDescription, shell_IPropertyDescription_GetSortDescription
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.GetSortDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The settings retrieved by this method are set through the <i>sortDescription</i> attribute of the <a href="https://msdn.microsoft.com/en-us/library/Bb773876(v=VS.85).aspx">labelInfo</a> element in the property's .propdesc file.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

