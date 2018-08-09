---
UID: NF:mmc.IExtendPropertySheet.CreatePropertyPages
title: IExtendPropertySheet::CreatePropertyPages
author: windows-sdk-content
description: Adds pages to a property sheet.
old-location: mmc\iextendpropertysheet_createpropertypages.htm
old-project: MMC
ms.assetid: 8B99EC8D-AFE1-4944-AF61-BFE93C0AF7DE
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreatePropertyPages, CreatePropertyPages method [MMC], CreatePropertyPages method [MMC],IExtendPropertySheet interface, IExtendPropertySheet interface [MMC],CreatePropertyPages method, IExtendPropertySheet.CreatePropertyPages, IExtendPropertySheet::CreatePropertyPages, mmc.iextendpropertysheet_createpropertypages, mmc/IExtendPropertySheet::CreatePropertyPages
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
req.idl: Mmc.idl
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
 - Mmc.h
api_name:
 - IExtendPropertySheet.CreatePropertyPages
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IExtendPropertySheet::CreatePropertyPages


## -description


Adds pages to a property sheet.


## -parameters




### -param lpProvider [in]

A pointer to the 
<a href="https://msdn.microsoft.com/e2115929-692e-4e59-bcdb-f37b02c53224">IPropertySheetCallback</a> interface.


### -param handle [in]

A value that specifies the handle used to route the 
<a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a> notification message to the appropriate 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> or 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface.

For snap-ins that use the 
<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a> interface directly, MMC creates the handle when the snap-in calls 
<a href="https://msdn.microsoft.com/f555dfd0-8af3-422f-a339-ab79daa89b45">IPropertySheetProvider::AddPrimaryPages</a> and specifies its bCreateHandle to be <b>TRUE</b>.


### -param lpIDataObject [in]

A pointer to the 
<a href="_ole_idataobject">IDataObject</a> interface on the object that contains context information about the scope or result item.


## -returns



This method can return one of these values.




## -remarks



The IPropertySheetCallback interface is passed to the snap-in during a call to this method. The lifetime of this interface is under the control of MMC. As such, the pointer lpIDataObject is valid only during the lifetime of the immediate call to this method. Caching the lpIDataObject pointer value outside of the callback is not recommended.

The handle specified by the handle parameter must be saved in the property page object to notify the parent of property changes using the API function 
<a href="https://msdn.microsoft.com/f563a6dd-22e7-4839-bd44-1702ab3e17a3">MMCPropertyChangeNotify</a>.

If the snap-in returns a success code (S_OK, S_FALSE) from 
CreatePropertyPages, then the snap-in must call 
MMCFreeNotifyHandle. If the snap-in returns an error code, then MMC immediately frees the handle. For more information about when 
MMCFreeNotifyHandle should be called, see 
<a href="https://msdn.microsoft.com/92802835-4324-4678-be9c-51dc9ca27576">MMCFreeNotifyHandle</a>.




## -see-also




<a href="https://msdn.microsoft.com/b41508bf-8399-44bb-abad-754aa5d32776">Adding Property Pages and Wizard Pages</a>



<a href="https://msdn.microsoft.com/c3c75e69-e16c-425b-bd8c-3c6f2e5ce2db">IExtendPropertySheet</a>



<a href="https://msdn.microsoft.com/e2115929-692e-4e59-bcdb-f37b02c53224">IPropertySheetCallback</a>



<a href="https://msdn.microsoft.com/92802835-4324-4678-be9c-51dc9ca27576">MMCFreeNotifyHandle</a>
 

 

