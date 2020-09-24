---
UID: NF:mmc.IExtendPropertySheet.QueryPagesFor
title: IExtendPropertySheet::QueryPagesFor (mmc.h)
description: Determines whether the object requires pages.
helpviewer_keywords: ["IExtendPropertySheet interface [MMC]","QueryPagesFor method","IExtendPropertySheet.QueryPagesFor","IExtendPropertySheet::QueryPagesFor","QueryPagesFor","QueryPagesFor method [MMC]","QueryPagesFor method [MMC]","IExtendPropertySheet interface","mmc.iextendpropertysheet_querypagesfor","mmc/IExtendPropertySheet::QueryPagesFor"]
old-location: mmc\iextendpropertysheet_querypagesfor.htm
tech.root: mmc
ms.assetid: F21A0AA2-8F79-4AEA-A5B1-8D650BE14C9F
ms.date: 12/05/2018
ms.keywords: IExtendPropertySheet interface [MMC],QueryPagesFor method, IExtendPropertySheet.QueryPagesFor, IExtendPropertySheet::QueryPagesFor, QueryPagesFor, QueryPagesFor method [MMC], QueryPagesFor method [MMC],IExtendPropertySheet interface, mmc.iextendpropertysheet_querypagesfor, mmc/IExtendPropertySheet::QueryPagesFor
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
 - IExtendPropertySheet::QueryPagesFor
 - mmc/IExtendPropertySheet::QueryPagesFor
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
 - IExtendPropertySheet.QueryPagesFor
---

# IExtendPropertySheet::QueryPagesFor


## -description

Determines whether the object requires pages.

## -parameters

### -param lpDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the object that contains context information about the scope or result item.

## -returns

This method can return one of these values.

## -remarks

The console calls this method to determine whether the 
<b>Properties</b> menu item should be added to the context menu.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/adding-property-pages-and-wizard-pages">Adding Property Pages and Wizard Pages</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendpropertysheet">IExtendPropertySheet</a>



<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetcallback">IPropertySheetCallback</a>