---
UID: NF:cmnquery.IQueryForm.AddForms
title: IQueryForm::AddForms (cmnquery.h)
description: Called to allow a query form extension object to add forms to the query dialog box.
helpviewer_keywords: ["AddForms","AddForms method [Active Directory]","AddForms method [Active Directory]","IQueryForm interface","IQueryForm interface [Active Directory]","AddForms method","IQueryForm.AddForms","IQueryForm::AddForms","_glines_iqueryform_addforms","ad.iqueryform__addforms","ad.iqueryform_addforms","cmnquery/IQueryForm::AddForms"]
old-location: ad\iqueryform_addforms.htm
tech.root: ad
ms.assetid: fadaa7e6-ccf2-42cd-a26e-19db107ce56c
ms.date: 12/05/2018
ms.keywords: AddForms, AddForms method [Active Directory], AddForms method [Active Directory],IQueryForm interface, IQueryForm interface [Active Directory],AddForms method, IQueryForm.AddForms, IQueryForm::AddForms, _glines_iqueryform_addforms, ad.iqueryform__addforms, ad.iqueryform_addforms, cmnquery/IQueryForm::AddForms
req.header: cmnquery.h
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
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryForm::AddForms
 - cmnquery/IQueryForm::AddForms
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IQueryForm.AddForms
---

# IQueryForm::AddForms


## -description

The <b>IQueryForm::AddForms</b> method is called to allow a query form extension object to add forms to the query dialog box.

## -parameters

### -param pAddFormsProc [in]

Pointer to a callback function of the form <a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddformsproc">CQAddFormsProc</a>. The query form extension  calls this function with the supplied <i>lParam</i> one time for each form to be added.

### -param lParam [in]

Contains a 32-bit value that is defined by the query handler. This value must be passed as the <i>lParam</i> parameter in the <a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddformsproc">CQAddFormsProc</a> call.

## -returns

Returns <b>S_OK</b> if successful or a standard <b>HRESULT</b> failure code otherwise.

## -see-also

<a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddformsproc">CQAddFormsProc</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-iqueryform">IQueryForm</a>