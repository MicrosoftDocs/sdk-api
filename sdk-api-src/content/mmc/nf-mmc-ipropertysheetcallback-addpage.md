---
UID: NF:mmc.IPropertySheetCallback.AddPage
title: IPropertySheetCallback::AddPage
author: windows-sdk-content
description: The IPropertySheetCallback::AddPage method enables a snap-in to add a page to a property sheet.
old-location: mmc\ipropertysheetcallback_addpage.htm
old-project: MMC
ms.assetid: db19fc38-7111-42f2-83a9-a08473a4d49b
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: AddPage, AddPage method [MMC], AddPage method [MMC],IPropertySheetCallback interface, IPropertySheetCallback interface [MMC],AddPage method, IPropertySheetCallback.AddPage, IPropertySheetCallback::AddPage, _slate_ipropertysheetcallback_addpage, mmc.ipropertysheetcallback_addpage, mmc/IPropertySheetCallback::AddPage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetCallback.AddPage
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IPropertySheetCallback::AddPage


## -description


The <b>IPropertySheetCallback::AddPage</b> method enables a snap-in to add a page to a property sheet.


## -parameters




### -param hPage [in]

A value that specifies the handle to the page to be added. The hPage parameter is a handle to a 
<a href="https://msdn.microsoft.com/28cbf3df-f345-4b4f-ac34-e32e63c9b6ec">PROPSHEETPAGE</a> structure created by the Windows API 
<a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a>.


## -returns



This method can return one of these values.




## -remarks



The snap-in cannot call 
AddPage from within a property page handler because the property page is created and runs on a secondary thread. A snap-in cannot call an MMC interface from a different thread than the one in which the snap-in was created. The correct place to call 
AddPage is in the snap-in's implementation of the 
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a> method.

If a snap-in uses the 
IPropertySheetProvider interface directly, it can use 
AddPage to add the primary pages and then call <a href="https://msdn.microsoft.com/f555dfd0-8af3-422f-a339-ab79daa89b45">IPropertySheetProvider::AddPrimaryPages</a> (<b>NULL</b>, <b>FALSE</b>, <b>NULL</b>, [<b>TRUE</b> or <b>FALSE</b>]) so that the provider will add these pages to the property sheet. For more information about how to create your property pages in the snap-in's implementation of 
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>, see <b>IPropertySheetProvider::AddPrimaryPages</b>.

Pages are added to the sheet in the order in which they are presented. The primary snap-in's pages are always added first.




## -see-also




<a href="https://msdn.microsoft.com/e2115929-692e-4e59-bcdb-f37b02c53224">IPropertySheetCallback</a>
 

 

