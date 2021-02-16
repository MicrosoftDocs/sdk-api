---
UID: NF:uiautomationcore.IGridProvider.get_ColumnCount
title: IGridProvider::get_ColumnCount (uiautomationcore.h)
description: Specifies the total number of columns in the grid.
helpviewer_keywords: ["ColumnCount property [Windows Accessibility]","ColumnCount property [Windows Accessibility]","IGridProvider interface","IGridProvider interface [Windows Accessibility]","ColumnCount property","IGridProvider.ColumnCount","IGridProvider.get_ColumnCount","IGridProvider::ColumnCount","IGridProvider::get_ColumnCount","get_ColumnCount","uiauto.uiauto_IGridProvider_ColumnCount","uiauto_IGridProvider_ColumnCount","uiautomationcore/IGridProvider::ColumnCount","uiautomationcore/IGridProvider::get_ColumnCount","winauto.uiauto_IGridProvider_ColumnCount"]
old-location: winauto\uiauto_IGridProvider_ColumnCount.htm
tech.root: WinAuto
ms.assetid: 8d180781-d797-4db4-82bd-92f3646da495
ms.date: 12/05/2018
ms.keywords: ColumnCount property [Windows Accessibility], ColumnCount property [Windows Accessibility],IGridProvider interface, IGridProvider interface [Windows Accessibility],ColumnCount property, IGridProvider.ColumnCount, IGridProvider.get_ColumnCount, IGridProvider::ColumnCount, IGridProvider::get_ColumnCount, get_ColumnCount, uiauto.uiauto_IGridProvider_ColumnCount, uiauto_IGridProvider_ColumnCount, uiautomationcore/IGridProvider::ColumnCount, uiautomationcore/IGridProvider::get_ColumnCount, winauto.uiauto_IGridProvider_ColumnCount
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
 - IGridProvider::get_ColumnCount
 - uiautomationcore/IGridProvider::get_ColumnCount
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
 - IGridProvider.ColumnCount
 - IGridProvider.get_ColumnCount
---

# IGridProvider::get_ColumnCount


## -description

Specifies the total number of columns in the grid.

This property is read-only.

## -parameters

## -remarks

Hidden rows and columns, depending on the provider implementation, may be loaded 
            in the logical tree and will therefore be reflected in the 
            <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igridprovider-get_rowcount">IGridProvider::RowCount</a> and 
            <b>IGridProvider::ColumnCount</b> properties. 
            If the hidden rows and columns have not yet been loaded they will not be counted.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igridprovider">IGridProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>