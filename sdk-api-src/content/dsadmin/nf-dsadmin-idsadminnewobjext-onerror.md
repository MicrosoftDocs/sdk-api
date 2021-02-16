---
UID: NF:dsadmin.IDsAdminNewObjExt.OnError
title: IDsAdminNewObjExt::OnError (dsadmin.h)
description: Called when an error has occurred in the wizard pages.
helpviewer_keywords: ["DSA_NEWOBJ_CTX_CLEANUP","DSA_NEWOBJ_CTX_COMMIT","DSA_NEWOBJ_CTX_POSTCOMMIT","DSA_NEWOBJ_CTX_PRECOMMIT","IDsAdminNewObjExt interface [Active Directory]","OnError method","IDsAdminNewObjExt.OnError","IDsAdminNewObjExt::OnError","OnError","OnError method [Active Directory]","OnError method [Active Directory]","IDsAdminNewObjExt interface","_glines_idsadminnewobjext_onerror","ad.idsadminnewobjext__onerror","ad.idsadminnewobjext_onerror","dsadmin/IDsAdminNewObjExt::OnError"]
old-location: ad\idsadminnewobjext_onerror.htm
tech.root: ad
ms.assetid: d1bb1eb6-db96-4322-8beb-0b9a3c6b0318
ms.date: 12/05/2018
ms.keywords: DSA_NEWOBJ_CTX_CLEANUP, DSA_NEWOBJ_CTX_COMMIT, DSA_NEWOBJ_CTX_POSTCOMMIT, DSA_NEWOBJ_CTX_PRECOMMIT, IDsAdminNewObjExt interface [Active Directory],OnError method, IDsAdminNewObjExt.OnError, IDsAdminNewObjExt::OnError, OnError, OnError method [Active Directory], OnError method [Active Directory],IDsAdminNewObjExt interface, _glines_idsadminnewobjext_onerror, ad.idsadminnewobjext__onerror, ad.idsadminnewobjext_onerror, dsadmin/IDsAdminNewObjExt::OnError
req.header: dsadmin.h
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
req.dll: DSAdmin.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsAdminNewObjExt::OnError
 - dsadmin/IDsAdminNewObjExt::OnError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNewObjExt.OnError
---

# IDsAdminNewObjExt::OnError


## -description

The <b>IDsAdminNewObjExt::OnError</b> method is called when an error has occurred in the wizard pages.

## -parameters

### -param hWnd [in]

The window handle used as the parent window for possible error messages.

### -param hr [in]

<b>HRESULT</b> of the error that occurred.

### -param uContext [in]

Specifies the context in which <b>OnError</b> is called. This will be one of the following values.



#### DSA_NEWOBJ_CTX_PRECOMMIT

An error occurred prior to the new object committed to persistent storage.



#### DSA_NEWOBJ_CTX_COMMIT

An error occurred while the new object was committed to persistent storage.



#### DSA_NEWOBJ_CTX_POSTCOMMIT

An error occurred after the new object was committed to persistent storage.



#### DSA_NEWOBJ_CTX_CLEANUP

An error occurred while the new object was committed to persistent storage.

## -returns

A primary creation extension returns <b>S_OK</b> to indicate that the error was handled by the extension or an OLE-defined error code to cause the system to display an error message.

The return value is ignored for a secondary creation extension.

## -see-also

<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjext">IDsAdminNewObjExt</a>