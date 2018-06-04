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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string retrieved by this method is determined by flags set in the <i>sortDescription</i> attribute of the <a href="shell.propdesc_schema_labelInfo">labelInfo</a> element in the property's .propdesc file.

It is the responsibility of the calling application to release <i>ppszDescription</i> when it is no longer needed.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

