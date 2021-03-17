---
UID: NF:dsadmin.IDsAdminCreateObj.Initialize
title: IDsAdminCreateObj::Initialize (dsadmin.h)
description: The IDsAdminCreateObj::Initialize method initializes an IDsAdminCreateObj object with data about the container where the object will be created, the class of the object to be created and, possibly, the source object to copy from.
helpviewer_keywords: ["IDsAdminCreateObj interface [Active Directory]","Initialize method","IDsAdminCreateObj.Initialize","IDsAdminCreateObj::Initialize","Initialize","Initialize method [Active Directory]","Initialize method [Active Directory]","IDsAdminCreateObj interface","_glines_idsadmincreateobj_initialize","ad.idsadmincreateobj__initialize","ad.idsadmincreateobj_initialize","dsadmin/IDsAdminCreateObj::Initialize"]
old-location: ad\idsadmincreateobj_initialize.htm
tech.root: ad
ms.assetid: 811863e7-25d2-48d0-bf97-61b49a224c98
ms.date: 12/05/2018
ms.keywords: IDsAdminCreateObj interface [Active Directory],Initialize method, IDsAdminCreateObj.Initialize, IDsAdminCreateObj::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IDsAdminCreateObj interface, _glines_idsadmincreateobj_initialize, ad.idsadmincreateobj__initialize, ad.idsadmincreateobj_initialize, dsadmin/IDsAdminCreateObj::Initialize
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
 - IDsAdminCreateObj::Initialize
 - dsadmin/IDsAdminCreateObj::Initialize
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
 - IDsAdminCreateObj.Initialize
---

# IDsAdminCreateObj::Initialize


## -description

The <b>IDsAdminCreateObj::Initialize</b> method initializes an 
<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadmincreateobj">IDsAdminCreateObj</a> object with data about the container where the object will be created, the class of the object to be created and, possibly, the source object to copy from.

## -parameters

### -param pADsContainerObj [in]

Pointer to an <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interface that represents the  container where the object will be created. This parameter must not be <b>NULL</b>.

### -param pADsCopySource [in]

Pointer to the <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a> interface of the object from which a copy is made. If the new object is not copied from another object, this parameter is <b>NULL</b>. The copy operation is only supported for user objects.

### -param lpszClassName [in]

Pointer to a <b>WCHAR</b> string that contains the LDAP name of the object class to be created. This parameter must not be <b>NULL</b>. Supported values are: "user", "computer", "printQueue", "group" and "contact".

## -returns

If the method succeeds, 
      <b>S_OK</b> is returned. If the method fails, an OLE-defined error code is returned.

## -remarks

The <b>IDsAdminCreateObj::Initialize</b> method must be called before <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadmincreateobj-createmodal">IDsAdminCreateObj::CreateModal</a> can be called.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadmincreateobj">IDsAdminCreateObj</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadmincreateobj-createmodal">IDsAdminCreateObj::CreateModal</a>