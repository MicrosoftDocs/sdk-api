---
UID: NF:propsys.IPropertyDescriptionAliasInfo.GetSortByAlias
title: IPropertyDescriptionAliasInfo::GetSortByAlias
author: windows-sdk-content
description: Gets the address of a pointer to the IPropertyDescription interface containing the primary sort column.
old-location: properties\IPropertyDescriptionAliasInfo_GetSortByAlias.htm
old-project: properties
ms.assetid: 22a60d4e-d7e7-4a14-a56a-5325a5dae2eb
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetSortByAlias, GetSortByAlias method [Windows Properties], GetSortByAlias method [Windows Properties],IPropertyDescriptionAliasInfo interface, IPropertyDescriptionAliasInfo interface [Windows Properties],GetSortByAlias method, IPropertyDescriptionAliasInfo.GetSortByAlias, IPropertyDescriptionAliasInfo::GetSortByAlias, _shell_IPropertyDescriptionAliasInfo_GetSortByAlias, properties.IPropertyDescriptionAliasInfo_GetSortByAlias, propsys/IPropertyDescriptionAliasInfo::GetSortByAlias, shell.IPropertyDescriptionAliasInfo_GetSortByAlias
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionAliasInfo.GetSortByAlias
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescriptionAliasInfo::GetSortByAlias


## -description


Gets the address of a pointer to the <a href="https://msdn.microsoft.com/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a> interface containing the primary sort column.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

A reference to the identifier of the requested <a href="https://msdn.microsoft.com/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a> interface.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the address of a pointer to the <a href="https://msdn.microsoft.com/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a> interface for the calling object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb761517(v=VS.85).aspx">IPropertyDescriptionAliasInfo</a>



<a href="shell.IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases">IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases</a>
 

 

