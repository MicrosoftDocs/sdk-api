---
UID: NC:cmnquery.LPCQADDFORMSPROC
title: LPCQADDFORMSPROC (cmnquery.h)
description: Called by a query form extension to add a form to the query dialog box.
helpviewer_keywords: ["CQAddFormsProc","CQAddFormsProc callback","CQAddFormsProc callback function [Active Directory]","LPCQADDFORMSPROC","LPCQADDFORMSPROC callback function pointer [Active Directory]","ad.cqaddformsproc","cmnquery/CQAddFormsProc"]
old-location: ad\cqaddformsproc.htm
tech.root: ad
ms.assetid: e4221299-93de-4747-b464-0d152d6e767b
ms.date: 12/05/2018
ms.keywords: CQAddFormsProc, CQAddFormsProc callback, CQAddFormsProc callback function [Active Directory], LPCQADDFORMSPROC, LPCQADDFORMSPROC callback function pointer [Active Directory], ad.cqaddformsproc, cmnquery/CQAddFormsProc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPCQADDFORMSPROC
 - cmnquery/LPCQADDFORMSPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cmnquery.h
api_name:
 - LPCQADDFORMSPROC
---

# LPCQADDFORMSPROC callback function


## -description

The <b>CQAddFormsProc</b> callback function is called by a query form extension to add a form to the query dialog box. A pointer to this function is supplied to the query form extension in the <i>pAddFormsProc</i> parameter of the <a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addforms">IQueryForm::AddForms</a> method. <b>CQAddFormsProc</b> is a placeholder for the query handler-defined function name.

## -parameters

### -param lParam

Contains a 32-bit value defined by the query handler. This value is passed to the query form extension as the <i>lParam</i> parameter in the <a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addforms">IQueryForm::AddForms</a> call.

### -param pForm

Pointer to a <a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqform">CQFORM</a> structure that defines the form to add.

## -returns

Returns an <b>HRESULT</b> value that indicates the success, or failure, of the form add operation. The following list lists possible return values.

## -see-also

<a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqform">CQFORM</a>



<a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addforms">IQueryForm::AddForms</a>