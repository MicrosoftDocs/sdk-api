---
UID: NF:mmc.IPropertySheetProvider.AddPrimaryPages
title: IPropertySheetProvider::AddPrimaryPages
author: windows-sdk-content
description: The IPropertySheetProvider::AddPrimaryPages method collects the pages from the primary snap-in.
old-location: mmc\ipropertysheetprovider_addprimarypages.htm
old-project: MMC
ms.assetid: f555dfd0-8af3-422f-a339-ab79daa89b45
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AddPrimaryPages, AddPrimaryPages method [MMC], AddPrimaryPages method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],AddPrimaryPages method, IPropertySheetProvider.AddPrimaryPages, IPropertySheetProvider::AddPrimaryPages, _slate_ipropertysheetprovider_addprimarypages, mmc.ipropertysheetprovider_addprimarypages, mmc/IPropertySheetProvider::AddPrimaryPages
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
 - IPropertySheetProvider.AddPrimaryPages
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IPropertySheetProvider::AddPrimaryPages


## -description


The <b>IPropertySheetProvider::AddPrimaryPages</b> method collects the pages from the primary snap-in.


## -parameters




### -param lpUnknown [in]

A pointer to snap-in interface that will be queried for the <b>IExtendPropertySheet</b> interface. If <i>bCreateHandle</i> is set to <b>TRUE</b>, this should also be a pointer to the snap-in's 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> or 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface that will be queried for <b>IExtendPropertySheet</b>. Be aware that this value can be <b>NULL</b>. See Remarks for details.


### -param bCreateHandle [in]

A value that specifies whether to create a console-provided notification handle that is used to route the <a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a> notification to the appropriate 
<b>IComponent</b> or 
<b>IComponentData</b> interface during calls to 
<a href="https://msdn.microsoft.com/f563a6dd-22e7-4839-bd44-1702ab3e17a3">MMCPropertyChangeNotify</a>. The notification handle is passed back to the snap-in during calls to the snap-in's implementation of the 
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a> method.

If <i>bCreateHandle</i> is set to <b>TRUE</b>, the <i>lpUnknown</i> parameter should be a pointer to the 
<b>IComponent</b> or 
<b>IComponentData</b> that receives the <a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a> notification.


### -param hNotifyWindow [in]

Reserved for future use. This value should be <b>NULL</b>.


### -param bScopePane [in]

Set to <b>TRUE</b> if the item is in the scope pane. Set to <b>FALSE</b> if it is in the result pane.


## -returns



This method can return one of these values.




## -remarks



The snap-in might not add any pages during this method call. If this is the case, extension pages should not be added.




## -see-also




<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a>



<a href="https://msdn.microsoft.com/5371b7ab-a298-44d1-99f1-1cd8f188cb91">Using IPropertySheetProvider Directly</a>
 

 

