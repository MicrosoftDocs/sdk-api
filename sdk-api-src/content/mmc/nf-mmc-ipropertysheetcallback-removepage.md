---
UID: NF:mmc.IPropertySheetCallback.RemovePage
title: IPropertySheetCallback::RemovePage
author: windows-sdk-content
description: The IPropertySheetCallback::RemovePage method enables a snap-in to remove a page from a property sheet.
old-location: mmc\ipropertysheetcallback_removepage.htm
old-project: MMC
ms.assetid: 2d54efbd-d88e-430e-9e46-c2b80559d356
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IPropertySheetCallback interface [MMC],RemovePage method, IPropertySheetCallback.RemovePage, IPropertySheetCallback::RemovePage, RemovePage, RemovePage method [MMC], RemovePage method [MMC],IPropertySheetCallback interface, _slate_ipropertysheetcallback_removepage, mmc.ipropertysheetcallback_removepage, mmc/IPropertySheetCallback::RemovePage
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
 - IPropertySheetCallback.RemovePage
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/e2115929-692e-4e59-bcdb-f37b02c53224">IPropertySheetCallback</a>
 

 

