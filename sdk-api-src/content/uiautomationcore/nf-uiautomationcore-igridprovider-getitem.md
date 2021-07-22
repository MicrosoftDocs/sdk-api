---
UID: NF:uiautomationcore.IGridProvider.GetItem
title: IGridProvider::GetItem (uiautomationcore.h)
description: Retrieves the Microsoft UI Automation provider for the specified cell.
helpviewer_keywords: ["GetItem","GetItem method [Windows Accessibility]","GetItem method [Windows Accessibility]","IGridProvider interface","IGridProvider interface [Windows Accessibility]","GetItem method","IGridProvider.GetItem","IGridProvider::GetItem","uiauto.uiauto_IGridProvider_GetItem","uiauto_IGridProvider_GetItem","uiautomationcore/IGridProvider::GetItem","winauto.uiauto_IGridProvider_GetItem"]
old-location: winauto\uiauto_IGridProvider_GetItem.htm
tech.root: WinAuto
ms.assetid: 5d62e872-c4a7-43c5-b5cf-5069ad46483a
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Accessibility], GetItem method [Windows Accessibility],IGridProvider interface, IGridProvider interface [Windows Accessibility],GetItem method, IGridProvider.GetItem, IGridProvider::GetItem, uiauto.uiauto_IGridProvider_GetItem, uiauto_IGridProvider_GetItem, uiautomationcore/IGridProvider::GetItem, winauto.uiauto_IGridProvider_GetItem
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
 - IGridProvider::GetItem
 - uiautomationcore/IGridProvider::GetItem
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
 - IGridProvider.GetItem
---

# IGridProvider::GetItem


## -description

Retrieves the Microsoft UI Automation provider for the specified cell.

## -parameters

### -param row [in]

Type: <b>int</b>

The ordinal number of the row of interest.

### -param column [in]

Type: <b>int</b>

The ordinal number of the column of interest.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>**</b>

Receives a pointer to a UI Automation provider for the specified cell or a null reference 
                (Nothing in Microsoft Visual Basic .NET) if the cell is empty.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).
            

If a cell is empty a UI Automation provider must still be 
            returned in order to support the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igriditemprovider-get_containinggrid">ContainingGrid</a> property 
            for that cell. This is possible when the layout of child elements in the grid is similar to a ragged array.
            

Hidden rows and columns, depending on the provider implementation, may be loaded in the 
            UI Automation tree and will therefore be reflected in the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igridprovider-get_rowcount">IGridProvider::RowCount</a> 
            and <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igridprovider-get_columncount">IGridProvider::ColumnCount</a> properties. 
            If the hidden rows and columns have not yet been loaded they should not be counted.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igridprovider">IGridProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>