---
UID: NF:uiautomationcore.IGridProvider.get_RowCount
title: IGridProvider::get_RowCount
author: windows-sdk-content
description: Specifies the total number of rows in the grid.
old-location: winauto\uiauto_IGridProvider_RowCount.htm
tech.root: WinAuto
ms.assetid: 036a05fd-53b7-4e6d-b96b-503832933b56
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IGridProvider interface [Windows Accessibility],RowCount property, IGridProvider.RowCount, IGridProvider.get_RowCount, IGridProvider::RowCount, IGridProvider::get_RowCount, RowCount property [Windows Accessibility], RowCount property [Windows Accessibility],IGridProvider interface, get_RowCount, uiauto.uiauto_IGridProvider_RowCount, uiauto_IGridProvider_RowCount, uiautomationcore/IGridProvider::RowCount, uiautomationcore/IGridProvider::get_RowCount, winauto.uiauto_IGridProvider_RowCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IGridProvider.RowCount
 - IGridProvider.get_RowCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
            <a href="https://msdn.microsoft.com/8d180781-d797-4db4-82bd-92f3646da495">IGridProvider::ColumnCount</a> properties. 
            If the hidden rows and columns have not yet been loaded they will not be counted.
            




## -see-also




<a href="https://msdn.microsoft.com/37e2cc95-d765-4c2c-ae8a-5a072a43ad5a">IGridProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

