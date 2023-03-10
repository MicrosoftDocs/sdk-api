---
UID: NF:dsadmin.IDsAdminNewObjExt.WriteData
title: IDsAdminNewObjExt::WriteData (dsadmin.h)
description: Enables the object creation wizard extension to write its data into an object in Active Directory Domain Services.
helpviewer_keywords: ["DSA_NEWOBJ_CTX_CLEANUP","DSA_NEWOBJ_CTX_POSTCOMMIT","DSA_NEWOBJ_CTX_PRECOMMIT","IDsAdminNewObjExt interface [Active Directory]","WriteData method","IDsAdminNewObjExt.WriteData","IDsAdminNewObjExt::WriteData","WriteData","WriteData method [Active Directory]","WriteData method [Active Directory]","IDsAdminNewObjExt interface","_glines_idsadminnewobjext_writedata","ad.idsadminnewobjext__writedata","ad.idsadminnewobjext_writedata","dsadmin/IDsAdminNewObjExt::WriteData"]
old-location: ad\idsadminnewobjext_writedata.htm
tech.root: ad
ms.assetid: 1788c124-c740-4f77-9687-63113d3b14a8
ms.date: 12/05/2018
ms.keywords: DSA_NEWOBJ_CTX_CLEANUP, DSA_NEWOBJ_CTX_POSTCOMMIT, DSA_NEWOBJ_CTX_PRECOMMIT, IDsAdminNewObjExt interface [Active Directory],WriteData method, IDsAdminNewObjExt.WriteData, IDsAdminNewObjExt::WriteData, WriteData, WriteData method [Active Directory], WriteData method [Active Directory],IDsAdminNewObjExt interface, _glines_idsadminnewobjext_writedata, ad.idsadminnewobjext__writedata, ad.idsadminnewobjext_writedata, dsadmin/IDsAdminNewObjExt::WriteData
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
 - IDsAdminNewObjExt::WriteData
 - dsadmin/IDsAdminNewObjExt::WriteData
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
 - IDsAdminNewObjExt.WriteData
---

# IDsAdminNewObjExt::WriteData


## -description

The <b>IDsAdminNewObjExt::WriteData</b> method enables the object creation wizard extension to write its data into an object in Active Directory Domain Services.

## -parameters

### -param hWnd [in]

The window handle used as the parent window for possible error messages.

### -param uContext [in]

Specifies the context in which <b>WriteData</b> is called. This will be one of the following values.



#### DSA_NEWOBJ_CTX_PRECOMMIT

<b>WriteData</b> is called prior to the new object committed to persistent storage. This is the context during which a secondary object creation extension should write its data.



#### DSA_NEWOBJ_CTX_POSTCOMMIT

<b>WriteData</b> is called after the new object has been committed to persistent storage.



#### DSA_NEWOBJ_CTX_CLEANUP

There has been a failure during the write process of the temporary object and the temporary object is recreated.

## -returns

Returns <b>S_OK</b> if successful or an OLE-defined error code otherwise.

## -remarks

A pointer to the temporary directory object is supplied to the extension when the <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-setobject">IDsAdminNewObjExt::SetObject</a> method is called.

A secondary object creation extension should not commit the data set during the <b>WriteData</b> method by calling <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>. The primary object creation extension will commit all of the data for the object when all of the extensions have added their data.

## -see-also

<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjext">IDsAdminNewObjExt</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-setobject">IDsAdminNewObjExt::SetObject</a>