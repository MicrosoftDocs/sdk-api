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

# IPropertyDescriptionAliasInfo::GetSortByAlias


## -description


Gets the address of a pointer to the <a href="shell.IPropertyDescription">IPropertyDescription</a> interface containing the primary sort column.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

A reference to the identifier of the requested <a href="shell.IPropertyDescription">IPropertyDescription</a> interface.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the address of a pointer to the <a href="shell.IPropertyDescription">IPropertyDescription</a> interface for the calling object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="shell.IPropertyDescriptionAliasInfo">IPropertyDescriptionAliasInfo</a>



<a href="shell.IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases">IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases</a>
 

 

