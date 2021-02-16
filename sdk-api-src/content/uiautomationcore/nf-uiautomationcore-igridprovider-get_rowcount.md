---
UID: NF:uiautomationcore.IGridProvider.get_RowCount
title: IGridProvider::get_RowCount (uiautomationcore.h)
description: Specifies the total number of rows in the grid.
helpviewer_keywords: ["IGridProvider interface [Windows Accessibility]","RowCount property","IGridProvider.RowCount","IGridProvider.get_RowCount","IGridProvider::RowCount","IGridProvider::get_RowCount","RowCount property [Windows Accessibility]","RowCount property [Windows Accessibility]","IGridProvider interface","get_RowCount","uiauto.uiauto_IGridProvider_RowCount","uiauto_IGridProvider_RowCount","uiautomationcore/IGridProvider::RowCount","uiautomationcore/IGridProvider::get_RowCount","winauto.uiauto_IGridProvider_RowCount"]
old-location: winauto\uiauto_IGridProvider_RowCount.htm
tech.root: WinAuto
ms.assetid: 036a05fd-53b7-4e6d-b96b-503832933b56
ms.date: 12/05/2018
ms.keywords: IGridProvider interface [Windows Accessibility],RowCount property, IGridProvider.RowCount, IGridProvider.get_RowCount, IGridProvider::RowCount, IGridProvider::get_RowCount, RowCount property [Windows Accessibility], RowCount property [Windows Accessibility],IGridProvider interface, get_RowCount, uiauto.uiauto_IGridProvider_RowCount, uiauto_IGridProvider_RowCount, uiautomationcore/IGridProvider::RowCount, uiautomationcore/IGridProvider::get_RowCount, winauto.uiauto_IGridProvider_RowCount
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGridProvider::get_RowCount
 - uiautomationcore/IGridProvider::get_RowCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IGridProvider.RowCount
 - IGridProvider.get_RowCount
---

# IGridProvider::get_RowCount


## -description

Specifies the total number of rows in the grid.

This property is read-only.

## -parameters

## -remarks

Hidden rows and columns, depending on the provider implementation, may be loaded 
            in the logical tree and will therefore be reflected in the 
            <b>IGridProvider::RowCount</b> and 
            <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igridprovider-get_columncount">IGridProvider::ColumnCount</a> properties. 
            If the hidden rows and columns have not yet been loaded they will not be counted.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igridprovider">IGridProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>