---
UID: NF:cmnquery.IQueryForm.AddPages
title: IQueryForm::AddPages (cmnquery.h)
description: Called to allow a query form object to add pages to an existing form.
helpviewer_keywords: ["AddPages","AddPages method [Active Directory]","AddPages method [Active Directory]","IQueryForm interface","IQueryForm interface [Active Directory]","AddPages method","IQueryForm.AddPages","IQueryForm::AddPages","_glines_iqueryform_addpages","ad.iqueryform__addpages","ad.iqueryform_addpages","cmnquery/IQueryForm::AddPages"]
old-location: ad\iqueryform_addpages.htm
tech.root: ad
ms.assetid: 797496fd-67db-4ec2-beec-224664d5d330
ms.date: 12/05/2018
ms.keywords: AddPages, AddPages method [Active Directory], AddPages method [Active Directory],IQueryForm interface, IQueryForm interface [Active Directory],AddPages method, IQueryForm.AddPages, IQueryForm::AddPages, _glines_iqueryform_addpages, ad.iqueryform__addpages, ad.iqueryform_addpages, cmnquery/IQueryForm::AddPages
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
 - IQueryForm::AddPages
 - cmnquery/IQueryForm::AddPages
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
 - IQueryForm.AddPages
---

# IQueryForm::AddPages


## -description

The <b>IQueryForm::AddPages</b> method is called to allow a query form object to add pages to an existing form.

## -parameters

### -param pAddPagesProc [in]

Pointer to a callback function of the form <a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddpagesproc">CQAddPagesProc</a>. The query form extension  calls this function with the supplied <i>lParam</i> one time for each page to be added to a form.

### -param lParam [in]

Contains a 32-bit value that is defined by the query handler. This value must be passed as the <i>lParam</i> parameter in the <a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddpagesproc">CQAddPagesProc</a> call.

## -returns

Returns <b>S_OK</b> if successful or a standard <b>HRESULT</b> failure code otherwise.

## -see-also

<a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddpagesproc">CQAddPagesProc</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-iqueryform">IQueryForm</a>