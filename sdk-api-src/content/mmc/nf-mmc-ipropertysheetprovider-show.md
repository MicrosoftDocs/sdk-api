---
UID: NF:mmc.IPropertySheetProvider.Show
title: IPropertySheetProvider::Show
author: windows-sdk-content
description: If the type that has been set in IPropertySheetProvider::CreatePropertySheet is a property sheet, IPropertySheetProvider::Show displays a property sheet frame that is parented to a hidden window.
old-location: mmc\ipropertysheetprovider_show.htm
old-project: MMC
ms.assetid: 08e1e3d9-9c9e-49c8-9d55-31c9519c5b0c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IPropertySheetProvider interface [MMC],Show method, IPropertySheetProvider.Show, IPropertySheetProvider::Show, Show, Show method [MMC], Show method [MMC],IPropertySheetProvider interface, _slate_ipropertysheetprovider_show, mmc.ipropertysheetprovider_show, mmc/IPropertySheetProvider::Show
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
 - IPropertySheetProvider.Show
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IPropertySheetProvider::Show


## -description


If the type that has been set in <a href="https://msdn.microsoft.com/8d53083a-d578-4a88-bd3f-d43c88d697e5">IPropertySheetProvider::CreatePropertySheet</a> is a property sheet, <b>IPropertySheetProvider::Show</b> displays a property sheet frame that is parented to a hidden window. If  the type that has been set in <b>IPropertySheetProvider::CreatePropertySheet</b> is a wizard, <b>IPropertySheetProvider::Show</b> displays a property sheet frame parented to the handle that is passed to this method.


## -parameters




### -param window [in]

A value that specifies the handle to the parent window.


### -param page [in]

A value that specifies which page on the property sheet is shown. It is zero-indexed.


## -returns



This method can return one of these values.




## -remarks



<b>IPropertySheetProvider::Show(
    –1, 0)</b> returns <b>E_FAIL</b>. This return code can be ignored in this case.

In situations in which the snap-in creates a property sheet in a call to <a href="https://msdn.microsoft.com/8d53083a-d578-4a88-bd3f-d43c88d697e5">IPropertySheetProvider::CreatePropertySheet</a>, optionally calls <a href="https://msdn.microsoft.com/f555dfd0-8af3-422f-a339-ab79daa89b45">IPropertySheetProvider::AddPrimaryPages</a> and <a href="https://msdn.microsoft.com/3a2ce7a6-65d6-4e39-b8b8-8d9b59b32d11">IPropertySheetProvider::AddExtensionPages</a>, and then decides not to show the property sheet, it should call <b>IPropertySheetProvider::Show(
    –1, 0)</b> to delete the property sheet and free its resources. In this case, the snap-in must delete the property page handles that it has created. This can be done before or after the snap-in calls <b>IPropertySheetProvider::Show(
    –1, 0)</b>, because MMC does not use the property page handles.

<b>IPropertySheetProvider::Show(
    –1, 0)</b> only deletes the current property sheet, that is, one that has been created, but is not yet shown. After a property sheet is shown, the snap-in cannot programmatically close it. Only the user can close a property sheet that is shown. In this case, MMC automatically deletes all associated property pages (<a href="https://msdn.microsoft.com/28cbf3df-f345-4b4f-ac34-e32e63c9b6ec">PROPSHEETPAGE</a> structures) provided by the snap-in.




## -see-also




<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a>
 

 

