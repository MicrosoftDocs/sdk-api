---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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



The settings retrieved by this method are set through the <i>sortDescription</i> attribute of the <a href="shell.propdesc_schema_labelInfo">labelInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

