---
UID: NF:mmc.IPropertySheetProvider.AddExtensionPages
title: IPropertySheetProvider::AddExtensionPages
author: windows-sdk-content
description: The IPropertySheetProvider::AddExtensionPages method collects the pages from the extension snap-ins.
old-location: mmc\ipropertysheetprovider_addextensionpages.htm
old-project: MMC
ms.assetid: 3a2ce7a6-65d6-4e39-b8b8-8d9b59b32d11
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: AddExtensionPages, AddExtensionPages method [MMC], AddExtensionPages method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],AddExtensionPages method, IPropertySheetProvider.AddExtensionPages, IPropertySheetProvider::AddExtensionPages, _slate_ipropertysheetprovider_addextensionpages, mmc.ipropertysheetprovider_addextensionpages, mmc/IPropertySheetProvider::AddExtensionPages
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
 - IPropertySheetProvider.AddExtensionPages
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IPropertySheetProvider::AddExtensionPages


## -description


The <b>IPropertySheetProvider::AddExtensionPages</b> method collects the pages from the extension snap-ins.


## -parameters






## -returns



This method can return one of these values.




## -remarks



Snap-ins that use the 
<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a> interface directly must add at least one page before extensions can add pages. They must also call the <b>IPropertySheetProvider::AddExtensionPages</b> method to allow extensions to add their own property pages.




## -see-also




<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a>
 

 

