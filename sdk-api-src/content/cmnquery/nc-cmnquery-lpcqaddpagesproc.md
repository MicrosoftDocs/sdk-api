---
UID: NC:cmnquery.LPCQADDPAGESPROC
title: LPCQADDPAGESPROC (cmnquery.h)
description: Called by a query form extension to add a page to a query form in the query dialog box.
helpviewer_keywords: ["CQAddPagesProc","CQAddPagesProc callback","CQAddPagesProc callback function [Active Directory]","LPCQADDPAGESPROC","LPCQADDPAGESPROC callback function pointer [Active Directory]","ad.cqaddpagesproc","cmnquery/CQAddPagesProc"]
old-location: ad\cqaddpagesproc.htm
tech.root: ad
ms.assetid: 2b62c1aa-ace7-4083-8eb3-7c5c499762c9
ms.date: 12/05/2018
ms.keywords: CQAddPagesProc, CQAddPagesProc callback, CQAddPagesProc callback function [Active Directory], LPCQADDPAGESPROC, LPCQADDPAGESPROC callback function pointer [Active Directory], ad.cqaddpagesproc, cmnquery/CQAddPagesProc
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
 - LPCQADDPAGESPROC
 - cmnquery/LPCQADDPAGESPROC
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
 - LPCQADDPAGESPROC
---

# LPCQADDPAGESPROC callback function


## -description

The <b>CQAddPagesProc</b> callback function is called by a query form extension to add a page to a query form in the query dialog box. A pointer to this function is supplied to the query form extension in the <i>pAddPagesProc</i> parameter of the <a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addpages">IQueryForm::AddPages</a> method. <b>CQAddPagesProc</b> is a placeholder for the query handler-defined function name.

## -parameters

### -param lParam

Contains a 32-bit value defined by the query handler. This value is passed to the query form extension as the <i>lParam</i> parameter in the <a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addpages">IQueryForm::AddPages</a> call.

### -param clsidForm

Contains the <b>CLSID</b> of the form that the page should be added to. This member can contain the <b>CLSID</b> of a custom query form or one of the system-supplied forms defined for the <b>clsidDefaultForm</b> member of the <a href="/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a> structure.

### -param pPage

Pointer to a <a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqpage">CQPAGE</a> structure that defines the page to be added.

## -returns

Returns an <b>HRESULT</b> value that indicates the success or failure of the page add operation. The following list lists possible return values.

## -see-also

<a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqpage">CQPAGE</a>



<a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addpages">IQueryForm::AddPages</a>



<a href="/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a>