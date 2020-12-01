---
UID: NF:mmc.IPropertySheetCallback.RemovePage
title: IPropertySheetCallback::RemovePage (mmc.h)
description: The IPropertySheetCallback::RemovePage method enables a snap-in to remove a page from a property sheet.
helpviewer_keywords: ["IPropertySheetCallback interface [MMC]","RemovePage method","IPropertySheetCallback.RemovePage","IPropertySheetCallback::RemovePage","RemovePage","RemovePage method [MMC]","RemovePage method [MMC]","IPropertySheetCallback interface","_slate_ipropertysheetcallback_removepage","mmc.ipropertysheetcallback_removepage","mmc/IPropertySheetCallback::RemovePage"]
old-location: mmc\ipropertysheetcallback_removepage.htm
tech.root: mmc
ms.assetid: 2d54efbd-d88e-430e-9e46-c2b80559d356
ms.date: 12/05/2018
ms.keywords: IPropertySheetCallback interface [MMC],RemovePage method, IPropertySheetCallback.RemovePage, IPropertySheetCallback::RemovePage, RemovePage, RemovePage method [MMC], RemovePage method [MMC],IPropertySheetCallback interface, _slate_ipropertysheetcallback_removepage, mmc.ipropertysheetcallback_removepage, mmc/IPropertySheetCallback::RemovePage
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
 - IPropertySheetCallback::RemovePage
 - mmc/IPropertySheetCallback::RemovePage
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
 - IPropertySheetCallback.RemovePage
---

# IPropertySheetCallback::RemovePage


## -description

The <b>IPropertySheetCallback::RemovePage</b> method enables a snap-in to remove a page from a property sheet.

## -parameters

### -param hPage [in]

A handle to the page to be removed.

## -returns

This method can return one of these values.

## -remarks

RemovePage can be used only for pages that the snap-in has added.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetcallback">IPropertySheetCallback</a>