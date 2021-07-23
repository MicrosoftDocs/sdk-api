---
UID: NN:cmnquery.IPersistQuery
title: IPersistQuery (cmnquery.h)
description: Used to store and retrieve query parameters to and from persistent storage.
helpviewer_keywords: ["IPersistQuery","IPersistQuery interface [Active Directory]","IPersistQuery interface [Active Directory]","described","_glines_ipersistquery","ad.ipersistquery","cmnquery/IPersistQuery"]
old-location: ad\ipersistquery.htm
tech.root: ad
ms.assetid: 9d90f119-3d10-4f06-bed4-5ffab9ae14a4
ms.date: 12/05/2018
ms.keywords: IPersistQuery, IPersistQuery interface [Active Directory], IPersistQuery interface [Active Directory],described, _glines_ipersistquery, ad.ipersistquery, cmnquery/IPersistQuery
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
 - IPersistQuery
 - cmnquery/IPersistQuery
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
 - IPersistQuery
---

# IPersistQuery interface


## -description

The <b>IPersistQuery</b> interface is used to store and retrieve query parameters to and from persistent storage.This storage pertains to the query parameters, not the results of a query. A pointer to this interface is provided to a query form extension in the <a href="/windows/desktop/AD/cqpm-persist">CQPM_PERSIST</a> message. An application can also provide its own  <b>IPersistQuery</b> implementation by passing a pointer to this interface to the query handler in the <b>pPersistQuery</b> member of the <a href="/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a> structure when <a href="/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a> is called.

## -inheritance

The <b>IPersistQuery</b> interface inherits from <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>. <b>IPersistQuery</b> also has these types of members:

## -see-also

<a href="/windows/desktop/AD/cqpm-persist">CQPM_PERSIST</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>



<a href="/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a>
