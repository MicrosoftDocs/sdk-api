---
UID: NF:mmc.IPropertySheetCallback.AddPage
title: IPropertySheetCallback::AddPage (mmc.h)
description: The IPropertySheetCallback::AddPage method enables a snap-in to add a page to a property sheet.
helpviewer_keywords: ["AddPage","AddPage method [MMC]","AddPage method [MMC]","IPropertySheetCallback interface","IPropertySheetCallback interface [MMC]","AddPage method","IPropertySheetCallback.AddPage","IPropertySheetCallback::AddPage","_slate_ipropertysheetcallback_addpage","mmc.ipropertysheetcallback_addpage","mmc/IPropertySheetCallback::AddPage"]
old-location: mmc\ipropertysheetcallback_addpage.htm
tech.root: mmc
ms.assetid: db19fc38-7111-42f2-83a9-a08473a4d49b
ms.date: 12/05/2018
ms.keywords: AddPage, AddPage method [MMC], AddPage method [MMC],IPropertySheetCallback interface, IPropertySheetCallback interface [MMC],AddPage method, IPropertySheetCallback.AddPage, IPropertySheetCallback::AddPage, _slate_ipropertysheetcallback_addpage, mmc.ipropertysheetcallback_addpage, mmc/IPropertySheetCallback::AddPage
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
 - IPropertySheetCallback::AddPage
 - mmc/IPropertySheetCallback::AddPage
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
 - IPropertySheetCallback.AddPage
---

# IPropertySheetCallback::AddPage


## -description

The <b>IPropertySheetCallback::AddPage</b> method enables a snap-in to add a page to a property sheet.

## -parameters

### -param hPage [in]

A value that specifies the handle to the page to be added. The hPage parameter is a handle to a 
<a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v3">PROPSHEETPAGE</a> structure created by the Windows API 
<a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>.

## -returns

This method can return one of these values.

## -remarks

The snap-in cannot call 
AddPage from within a property page handler because the property page is created and runs on a secondary thread. A snap-in cannot call an MMC interface from a different thread than the one in which the snap-in was created. The correct place to call 
AddPage is in the snap-in's implementation of the 
<a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a> method.

If a snap-in uses the 
IPropertySheetProvider interface directly, it can use 
AddPage to add the primary pages and then call <a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addprimarypages">IPropertySheetProvider::AddPrimaryPages</a> (<b>NULL</b>, <b>FALSE</b>, <b>NULL</b>, [<b>TRUE</b> or <b>FALSE</b>]) so that the provider will add these pages to the property sheet. For more information about how to create your property pages in the snap-in's implementation of 
<a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a>, see <b>IPropertySheetProvider::AddPrimaryPages</b>.

Pages are added to the sheet in the order in which they are presented. The primary snap-in's pages are always added first.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetcallback">IPropertySheetCallback</a>