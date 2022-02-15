---
UID: NF:mmc.IPropertySheetProvider.AddExtensionPages
title: IPropertySheetProvider::AddExtensionPages (mmc.h)
description: The IPropertySheetProvider::AddExtensionPages method collects the pages from the extension snap-ins.
helpviewer_keywords: ["AddExtensionPages","AddExtensionPages method [MMC]","AddExtensionPages method [MMC]","IPropertySheetProvider interface","IPropertySheetProvider interface [MMC]","AddExtensionPages method","IPropertySheetProvider.AddExtensionPages","IPropertySheetProvider::AddExtensionPages","_slate_ipropertysheetprovider_addextensionpages","mmc.ipropertysheetprovider_addextensionpages","mmc/IPropertySheetProvider::AddExtensionPages"]
old-location: mmc\ipropertysheetprovider_addextensionpages.htm
tech.root: mmc
ms.assetid: 3a2ce7a6-65d6-4e39-b8b8-8d9b59b32d11
ms.date: 12/05/2018
ms.keywords: AddExtensionPages, AddExtensionPages method [MMC], AddExtensionPages method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],AddExtensionPages method, IPropertySheetProvider.AddExtensionPages, IPropertySheetProvider::AddExtensionPages, _slate_ipropertysheetprovider_addextensionpages, mmc.ipropertysheetprovider_addextensionpages, mmc/IPropertySheetProvider::AddExtensionPages
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertySheetProvider::AddExtensionPages
 - mmc/IPropertySheetProvider::AddExtensionPages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider.AddExtensionPages
---

# IPropertySheetProvider::AddExtensionPages


## -description

The <b>IPropertySheetProvider::AddExtensionPages</b> method collects the pages from the extension snap-ins.



## -returns

This method can return one of these values.

## -remarks

Snap-ins that use the 
<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetprovider">IPropertySheetProvider</a> interface directly must add at least one page before extensions can add pages. They must also call the <b>IPropertySheetProvider::AddExtensionPages</b> method to allow extensions to add their own property pages.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetprovider">IPropertySheetProvider</a>
