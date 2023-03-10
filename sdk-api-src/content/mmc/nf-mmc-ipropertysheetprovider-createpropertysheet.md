---
UID: NF:mmc.IPropertySheetProvider.CreatePropertySheet
title: IPropertySheetProvider::CreatePropertySheet (mmc.h)
description: Creates a property sheet frame.
helpviewer_keywords: ["CreatePropertySheet","CreatePropertySheet method [MMC]","CreatePropertySheet method [MMC]","IPropertySheetProvider interface","IPropertySheetProvider interface [MMC]","CreatePropertySheet method","IPropertySheetProvider.CreatePropertySheet","IPropertySheetProvider::CreatePropertySheet","MMC_PSO_HASHELP","MMC_PSO_NEWWIZARDTYPE","MMC_PSO_NOAPPLYNOW","MMC_PSO_NO_PROPTITLE","_slate_ipropertysheetprovider_createpropertysheet","mmc.ipropertysheetprovider_createpropertysheet","mmc/IPropertySheetProvider::CreatePropertySheet"]
old-location: mmc\ipropertysheetprovider_createpropertysheet.htm
tech.root: mmc
ms.assetid: 8d53083a-d578-4a88-bd3f-d43c88d697e5
ms.date: 12/05/2018
ms.keywords: CreatePropertySheet, CreatePropertySheet method [MMC], CreatePropertySheet method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],CreatePropertySheet method, IPropertySheetProvider.CreatePropertySheet, IPropertySheetProvider::CreatePropertySheet, MMC_PSO_HASHELP, MMC_PSO_NEWWIZARDTYPE, MMC_PSO_NOAPPLYNOW, MMC_PSO_NO_PROPTITLE, _slate_ipropertysheetprovider_createpropertysheet, mmc.ipropertysheetprovider_createpropertysheet, mmc/IPropertySheetProvider::CreatePropertySheet
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertySheetProvider::CreatePropertySheet
 - mmc/IPropertySheetProvider::CreatePropertySheet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider.CreatePropertySheet
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

### -param pIDataObjectm [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object for the cookie. If the value of this parameter is <b>NULL</b>, MMC will not call any of the 
IExtendPropertySheet2 methods implemented by extension snap-ins.

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

## -returns

This method can return one of these values.

## -remarks

This method creates an object that collects all information required to create a property sheet. If the 
CreatePropertySheet call is successful, but subsequent errors occur, you must call 
<a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-show">IPropertySheetProvider::Show</a>(
    –1, 0) to free objects. The return code can be ignored in this case.

In situations in which the snap-in creates a property sheet in a call to <b>IPropertySheetProvider::CreatePropertySheet</b> and then optionally calls <a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addprimarypages">IPropertySheetProvider::AddPrimaryPages</a> and <a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addextensionpages">IPropertySheetProvider::AddExtensionPages</a>, and then decides not to show the property sheet, it should call <a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-show">IPropertySheetProvider::Show</a>(
    –1, 0) to delete the property sheet and free its resources. In this case, the snap-in must delete the property page handles it has created. This can be done before or after the snap-in calls <b>IPropertySheetProvider::Show</b>(
    –1, 0), because MMC does not use the property page handles.

For a snap-in that targets MMC 1.1, the snap-in must keep an extra reference on the IDataObject interface that it passes to MMC in the <b>IPropertySheetProvider::CreatePropertySheet</b> call. This reference must be kept from before the <b>IPropertySheetProvider::CreatePropertySheet</b> call until after the property sheet is possibly closed with a call to <a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-show">IPropertySheetProvider::Show</a>(
    –1, 0).

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetprovider">IPropertySheetProvider</a>



<a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-show">IPropertySheetProvider::Show</a>