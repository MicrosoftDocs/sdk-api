---
UID: NF:shobjidl_core.IFolderViewSettings.GetGroupByProperty
title: IFolderViewSettings::GetGroupByProperty (shobjidl_core.h)
author: windows-sdk-content
description: Gets a grouping property.
old-location: shell\IFolderViewSettings_GetGroupByProperty.htm
tech.root: shell
ms.assetid: 5a5fb679-f2e7-457f-9624-64ed993c2d74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGroupByProperty, GetGroupByProperty method [Windows Shell], GetGroupByProperty method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetGroupByProperty method, IFolderViewSettings.GetGroupByProperty, IFolderViewSettings::GetGroupByProperty, _shell_IFolderViewSettings_GetGroupByProperty, shell.IFolderViewSettings_GetGroupByProperty, shobjidl_core/IFolderViewSettings::GetGroupByProperty
ms.topic: method
f1_keywords:
- shobjidl_core/IFolderViewSettings.GetGroupByProperty
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- shobjidl_core.h
api_name:
- IFolderViewSettings.GetGroupByProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderViewSettings::GetGroupByProperty


## -description


Gets a grouping property.


## -parameters




### -param pkey [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure indicating the key by which content is grouped.


### -param pfGroupAscending [out]

Type: <b>BOOL*</b>

A pointer to a value indicating whether grouping order is ascending.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



