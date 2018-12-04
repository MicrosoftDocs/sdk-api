---
UID: NF:propsys.IPropertyDescription.GetSortDescriptionLabel
title: IPropertyDescription::GetSortDescriptionLabel
author: windows-sdk-content
description: Gets the localized display string that describes the current sort order.
old-location: properties\IPropertyDescription_GetSortDescriptionLabel.htm
tech.root: properties
ms.assetid: 5cfa445b-953b-474f-ba7b-1ed6cfbf981d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetSortDescriptionLabel, GetSortDescriptionLabel method [Windows Properties], GetSortDescriptionLabel method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetSortDescriptionLabel method, IPropertyDescription.GetSortDescriptionLabel, IPropertyDescription::GetSortDescriptionLabel, properties.IPropertyDescription_GetSortDescriptionLabel, propsys/IPropertyDescription::GetSortDescriptionLabel, shell.IPropertyDescription_GetSortDescriptionLabel, shell_IPropertyDescription_GetSortDescriptionLabel
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPropertyDescription.GetSortDescriptionLabel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

