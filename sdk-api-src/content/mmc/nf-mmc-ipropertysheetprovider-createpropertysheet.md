---
UID: NF:mmc.IPropertySheetProvider.CreatePropertySheet
title: IPropertySheetProvider::CreatePropertySheet
author: windows-sdk-content
description: Creates a property sheet frame.
old-location: mmc\ipropertysheetprovider_createpropertysheet.htm
tech.root: mmc
ms.assetid: 8d53083a-d578-4a88-bd3f-d43c88d697e5
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: CreatePropertySheet, CreatePropertySheet method [MMC], CreatePropertySheet method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],CreatePropertySheet method, IPropertySheetProvider.CreatePropertySheet, IPropertySheetProvider::CreatePropertySheet, MMC_PSO_HASHELP, MMC_PSO_NEWWIZARDTYPE, MMC_PSO_NOAPPLYNOW, MMC_PSO_NO_PROPTITLE, _slate_ipropertysheetprovider_createpropertysheet, mmc.ipropertysheetprovider_createpropertysheet, mmc/IPropertySheetProvider::CreatePropertySheet
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider.CreatePropertySheet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertySheetProvider::CreatePropertySheet


## -description


The <b>IPropertySheetProvider::CreatePropertySheet</b> method creates a property sheet frame.


## -parameters




### -param title [in]

A pointer to a null-terminated string that contains the title of the property page. This parameter cannot be <b>NULL</b>.


### -param type [in]

<b>TRUE</b> creates a property sheet and <b>FALSE</b> creates a wizard.


### -param cookie [in]

Cookie value of the currently selected item. This can be <b>NULL</b> when 
CreatePropertySheet is called by an extension snap-in.


### -param pIDataObjectm

TBD


### -param dwOptions [in]

A value that specifies the flags that can be set by the method call. The parameter can be a combination of the following values:



#### MMC_PSO_NOAPPLYNOW

Remove Apply Now button.



#### MMC_PSO_HASHELP

Add a 
<b>Help</b> button.



#### MMC_PSO_NO_PROPTITLE

Ignored for wizards. For property sheets, if this option is specified, then the words "Properties for" will not be inserted at the beginning of the property sheet title bar.



#### MMC_PSO_NEWWIZARDTYPE

Use Wizard 97 style.

For example, to create a property sheet that has a 
<b>Help</b> button and that does not have an Apply Now button, the dwOptions parameter should be <code>MMC_PSO_NOAPPLYNOW | MMC_PSO_HASHELP</code>.


#### - pIDataObject [in]

A pointer to the 
<a href="_ole_idataobject">IDataObject</a> interface on the data object for the cookie. If the value of this parameter is <b>NULL</b>, MMC will not call any of the 
IExtendPropertySheet2 methods implemented by extension snap-ins.


## -returns



This method can return one of these values.




## -remarks



This method creates an object that collects all information required to create a property sheet. If the 
CreatePropertySheet call is successful, but subsequent errors occur, you must call 
<a href="https://msdn.microsoft.com/08e1e3d9-9c9e-49c8-9d55-31c9519c5b0c">IPropertySheetProvider::Show</a>(
    –1, 0) to free objects. The return code can be ignored in this case.

In situations in which the snap-in creates a property sheet in a call to <b>IPropertySheetProvider::CreatePropertySheet</b> and then optionally calls <a href="https://msdn.microsoft.com/f555dfd0-8af3-422f-a339-ab79daa89b45">IPropertySheetProvider::AddPrimaryPages</a> and <a href="https://msdn.microsoft.com/3a2ce7a6-65d6-4e39-b8b8-8d9b59b32d11">IPropertySheetProvider::AddExtensionPages</a>, and then decides not to show the property sheet, it should call <a href="https://msdn.microsoft.com/08e1e3d9-9c9e-49c8-9d55-31c9519c5b0c">IPropertySheetProvider::Show</a>(
    –1, 0) to delete the property sheet and free its resources. In this case, the snap-in must delete the property page handles it has created. This can be done before or after the snap-in calls <b>IPropertySheetProvider::Show</b>(
    –1, 0), because MMC does not use the property page handles.

For a snap-in that targets MMC 1.1, the snap-in must keep an extra reference on the IDataObject interface that it passes to MMC in the <b>IPropertySheetProvider::CreatePropertySheet</b> call. This reference must be kept from before the <b>IPropertySheetProvider::CreatePropertySheet</b> call until after the property sheet is possibly closed with a call to <a href="https://msdn.microsoft.com/08e1e3d9-9c9e-49c8-9d55-31c9519c5b0c">IPropertySheetProvider::Show</a>(
    –1, 0).




## -see-also




<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a>



<a href="https://msdn.microsoft.com/08e1e3d9-9c9e-49c8-9d55-31c9519c5b0c">IPropertySheetProvider::Show</a>
 

 

