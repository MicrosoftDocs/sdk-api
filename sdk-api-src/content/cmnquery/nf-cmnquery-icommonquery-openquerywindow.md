---
UID: NF:cmnquery.ICommonQuery.OpenQueryWindow
title: ICommonQuery::OpenQueryWindow (cmnquery.h)
description: The ICommonQuery::OpenQueryWindow method displays the directory service query dialog. This method does not return until the dialog box has been closed by the user.
helpviewer_keywords: ["CFSTR_DSOBJECTNAMES","CFSTR_DSQUERYPARAMS","CFSTR_DSQUERYSCOPE","ICommonQuery interface [Active Directory]","OpenQueryWindow method","ICommonQuery.OpenQueryWindow","ICommonQuery::OpenQueryWindow","OpenQueryWindow","OpenQueryWindow method [Active Directory]","OpenQueryWindow method [Active Directory]","ICommonQuery interface","_glines_icommonquery_openquerywindow","ad.icommonquery__openquerywindow","ad.icommonquery_openquerywindow","cmnquery/ICommonQuery::OpenQueryWindow"]
old-location: ad\icommonquery_openquerywindow.htm
tech.root: ad
ms.assetid: 604c4d7a-1f85-4e5b-9879-be502c5c7bff
ms.date: 12/05/2018
ms.keywords: CFSTR_DSOBJECTNAMES, CFSTR_DSQUERYPARAMS, CFSTR_DSQUERYSCOPE, ICommonQuery interface [Active Directory],OpenQueryWindow method, ICommonQuery.OpenQueryWindow, ICommonQuery::OpenQueryWindow, OpenQueryWindow, OpenQueryWindow method [Active Directory], OpenQueryWindow method [Active Directory],ICommonQuery interface, _glines_icommonquery_openquerywindow, ad.icommonquery__openquerywindow, ad.icommonquery_openquerywindow, cmnquery/ICommonQuery::OpenQueryWindow
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
 - ICommonQuery::OpenQueryWindow
 - cmnquery/ICommonQuery::OpenQueryWindow
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
 - ICommonQuery.OpenQueryWindow
---

# ICommonQuery::OpenQueryWindow


## -description

The <b>ICommonQuery::OpenQueryWindow</b> method displays the directory service query dialog. This method does not return until the dialog box has been closed by the user.

## -parameters

### -param hwndParent [in]

Contains the handle of the window to use as the parent to the query dialog box. This parameter can be <b>NULL</b> if no parent is specified.

### -param pQueryWnd [in]

Address of an 
<a href="/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a> structure that defines the query to perform and the characteristics of the query dialog.

### -param ppDataObject [out]

Address of an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface pointer that receives the results of the query. This parameter only receives valid data if this method returns <b>S_OK</b>. This <b>IDataObject</b> supports the following clipboard formats.



#### CFSTR_DSOBJECTNAMES

Contains data about  objects selected in the directory service query dialog box.



#### CFSTR_DSQUERYPARAMS

Contains data about the query performed by the directory service query dialog box.



#### CFSTR_DSQUERYSCOPE

Contains data about the scope of the query performed by the directory service query dialog box.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -see-also

<a href="/windows/desktop/AD/cfstr-dsobjectnames">CFSTR_DSOBJECTNAMES</a>



<a href="/windows/desktop/AD/cfstr-dsqueryparams">CFSTR_DSQUERYPARAMS</a>



<a href="/windows/desktop/AD/cfstr-dsqueryscope">CFSTR_DSQUERYSCOPE</a>



<a href="/windows/desktop/api/dsquery/ns-dsquery-dsqueryinitparams">DSQUERYINITPARAMS</a>



<a href="/windows/desktop/api/dsquery/ns-dsquery-dsqueryparams">DSQUERYPARAMS</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-icommonquery">ICommonQuery</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a>