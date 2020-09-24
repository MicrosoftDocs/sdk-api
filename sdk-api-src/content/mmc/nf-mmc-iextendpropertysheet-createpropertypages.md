---
UID: NF:mmc.IExtendPropertySheet.CreatePropertyPages
title: IExtendPropertySheet::CreatePropertyPages (mmc.h)
description: Adds pages to a property sheet.
helpviewer_keywords: ["CreatePropertyPages","CreatePropertyPages method [MMC]","CreatePropertyPages method [MMC]","IExtendPropertySheet interface","IExtendPropertySheet interface [MMC]","CreatePropertyPages method","IExtendPropertySheet.CreatePropertyPages","IExtendPropertySheet::CreatePropertyPages","mmc.iextendpropertysheet_createpropertypages","mmc/IExtendPropertySheet::CreatePropertyPages"]
old-location: mmc\iextendpropertysheet_createpropertypages.htm
tech.root: mmc
ms.assetid: 8B99EC8D-AFE1-4944-AF61-BFE93C0AF7DE
ms.date: 12/05/2018
ms.keywords: CreatePropertyPages, CreatePropertyPages method [MMC], CreatePropertyPages method [MMC],IExtendPropertySheet interface, IExtendPropertySheet interface [MMC],CreatePropertyPages method, IExtendPropertySheet.CreatePropertyPages, IExtendPropertySheet::CreatePropertyPages, mmc.iextendpropertysheet_createpropertypages, mmc/IExtendPropertySheet::CreatePropertyPages
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtendPropertySheet::CreatePropertyPages
 - mmc/IExtendPropertySheet::CreatePropertyPages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendPropertySheet.CreatePropertyPages
---

# IExtendPropertySheet::CreatePropertyPages


## -description

Adds pages to a property sheet.

## -parameters

### -param lpProvider [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetcallback">IPropertySheetCallback</a> interface.

### -param handle [in]

A value that specifies the handle used to route the 
<a href="/previous-versions/windows/desktop/mmc/mmcn-property-change">MMCN_PROPERTY_CHANGE</a> notification message to the appropriate 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> or 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface.

For snap-ins that use the 
<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetprovider">IPropertySheetProvider</a> interface directly, MMC creates the handle when the snap-in calls 
<a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addprimarypages">IPropertySheetProvider::AddPrimaryPages</a> and specifies its bCreateHandle to be <b>TRUE</b>.

### -param lpIDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the object that contains context information about the scope or result item.

## -returns

This method can return one of these values.

## -remarks

The IPropertySheetCallback interface is passed to the snap-in during a call to this method. The lifetime of this interface is under the control of MMC. As such, the pointer lpIDataObject is valid only during the lifetime of the immediate call to this method. Caching the lpIDataObject pointer value outside of the callback is not recommended.

The handle specified by the handle parameter must be saved in the property page object to notify the parent of property changes using the API function 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertychangenotify">MMCPropertyChangeNotify</a>.

If the snap-in returns a success code (S_OK, S_FALSE) from 
CreatePropertyPages, then the snap-in must call 
MMCFreeNotifyHandle. If the snap-in returns an error code, then MMC immediately frees the handle. For more information about when 
MMCFreeNotifyHandle should be called, see 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcfreenotifyhandle">MMCFreeNotifyHandle</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/adding-property-pages-and-wizard-pages">Adding Property Pages and Wizard Pages</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendpropertysheet">IExtendPropertySheet</a>



<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetcallback">IPropertySheetCallback</a>



<a href="/windows/desktop/api/mmc/nf-mmc-mmcfreenotifyhandle">MMCFreeNotifyHandle</a>