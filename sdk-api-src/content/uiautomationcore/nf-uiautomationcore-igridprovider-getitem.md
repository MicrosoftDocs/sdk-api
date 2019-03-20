---
UID: NF:uiautomationcore.IGridProvider.GetItem
title: IGridProvider::GetItem (uiautomationcore.h)
author: windows-sdk-content
description: Retrieves the Microsoft UI Automation provider for the specified cell.
old-location: winauto\uiauto_IGridProvider_GetItem.htm
tech.root: WinAuto
ms.assetid: 5d62e872-c4a7-43c5-b5cf-5069ad46483a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetItem, GetItem method [Windows Accessibility], GetItem method [Windows Accessibility],IGridProvider interface, IGridProvider interface [Windows Accessibility],GetItem method, IGridProvider.GetItem, IGridProvider::GetItem, uiauto.uiauto_IGridProvider_GetItem, uiauto_IGridProvider_GetItem, uiautomationcore/IGridProvider::GetItem, winauto.uiauto_IGridProvider_GetItem
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IGridProvider.GetItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>**</b>

Receives a pointer to a UI Automation provider for the specified cell or a null reference 
                (Nothing in Microsoft Visual Basic .NET) if the cell is empty.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).
            

If a cell is empty a UI Automation provider must still be 
            returned in order to support the <a href="https://msdn.microsoft.com/760abeea-e432-49e3-a2df-0f6f30b029f0">ContainingGrid</a> property 
            for that cell. This is possible when the layout of child elements in the grid is similar to a ragged array.
            

Hidden rows and columns, depending on the provider implementation, may be loaded in the 
            UI Automation tree and will therefore be reflected in the <a href="https://msdn.microsoft.com/036a05fd-53b7-4e6d-b96b-503832933b56">IGridProvider::RowCount</a> 
            and <a href="https://msdn.microsoft.com/8d180781-d797-4db4-82bd-92f3646da495">IGridProvider::ColumnCount</a> properties. 
            If the hidden rows and columns have not yet been loaded they should not be counted.
            




## -see-also




<a href="https://msdn.microsoft.com/37e2cc95-d765-4c2c-ae8a-5a072a43ad5a">IGridProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

