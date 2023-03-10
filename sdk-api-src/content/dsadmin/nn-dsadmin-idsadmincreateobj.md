---
UID: NN:dsadmin.IDsAdminCreateObj
title: IDsAdminCreateObj (dsadmin.h)
description: Used by an application or component to programmatically start a creation wizard for a specified object class.
helpviewer_keywords: ["IDsAdminCreateObj","IDsAdminCreateObj interface [Active Directory]","IDsAdminCreateObj interface [Active Directory]","described","_glines_idsadmincreateobj","ad.idsadmincreateobj","dsadmin/IDsAdminCreateObj"]
old-location: ad\idsadmincreateobj.htm
tech.root: ad
ms.assetid: 93673b29-744a-4100-86b7-8a2eec861c47
ms.date: 12/05/2018
ms.keywords: IDsAdminCreateObj, IDsAdminCreateObj interface [Active Directory], IDsAdminCreateObj interface [Active Directory],described, _glines_idsadmincreateobj, ad.idsadmincreateobj, dsadmin/IDsAdminCreateObj
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
 - IDsAdminCreateObj
 - dsadmin/IDsAdminCreateObj
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
 - IDsAdminCreateObj
---

# IDsAdminCreateObj interface


## -description

The <b>IDsAdminCreateObj</b> interface is implemented by the system and used by an application or component to programmatically start a creation wizard for a specified object class.

To obtain an instance of this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsAdminCreateObj</b> class identifier as shown below.

```cpp
#include <initguid.h>
#include <dsadmin.h>

HRESULT hr = S_OK;
IDsAdminCreateObj* pCreateObj = NULL;
hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
        NULL, CLSCTX_INPROC_SERVER,
        IID_IDsAdminCreateObj,
        (void**)&pCreateObj);
```

## -inheritance

The <b>IDsAdminCreateObj</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminCreateObj</b> also has these types of members:

## -see-also

<a href="/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/AD/invoking-creation-wizards-from-your-application">Invoking Creation Wizards from Your Application</a>
