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

# IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases


## -description


Gets the address of a pointer to the <a href="shell.IPropertyDescriptionList">IPropertyDescriptionList</a> interface, which contains additional sort column values.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

A reference to the identifier of the requested <a href="shell.IPropertyDescriptionList">IPropertyDescriptionList</a> interface.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the address of a pointer to an <a href="shell.IPropertyDescriptionList">IPropertyDescriptionList</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The following is an example usage for this method. When sorting by System.Author: System.DateModified, System.DateCreated, and System.ItemNameDisplay may be used as secondary sort columns.  This ensures a unique sort order (for System.Author) and is used to provide a more consistent user experience.


 Calling applications include any UI that wants the secondary sort columns for a given property.




## -see-also




<a href="shell.IPropertyDescriptionAliasInfo">IPropertyDescriptionAliasInfo</a>



<a href="shell.IPropertyDescriptionAliasInfo_GetSortByAlias">IPropertyDescriptionAliasInfo::GetSortByAlias</a>
 

 

