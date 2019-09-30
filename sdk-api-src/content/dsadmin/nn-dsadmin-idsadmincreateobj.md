---
UID: NN:dsadmin.IDsAdminCreateObj
title: IDsAdminCreateObj (dsadmin.h)
author: windows-sdk-content
description: Used by an application or component to programmatically start a creation wizard for a specified object class.
old-location: ad\idsadmincreateobj.htm
tech.root: ad
ms.assetid: 93673b29-744a-4100-86b7-8a2eec861c47
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDsAdminCreateObj, IDsAdminCreateObj interface [Active Directory], IDsAdminCreateObj interface [Active Directory],described, _glines_idsadmincreateobj, ad.idsadmincreateobj, dsadmin/IDsAdminCreateObj
ms.topic: interface
f1_keywords: 
 - "dsadmin/IDsAdminCreateObj"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminCreateObj
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsAdminCreateObj interface


## -description


The <b>IDsAdminCreateObj</b> interface is implemented by the system and used by an application or component to programmatically start a creation wizard for a specified object class.

To obtain an instance of this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsAdminCreateObj</b> class identifier as shown below.

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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminCreateObj</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminCreateObj</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsAdminCreateObj</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadmincreateobj-createmodal">CreateModal</a>
</td>
<td align="left" width="63%">
Displays the creation wizard and returns the newly created object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadmincreateobj-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the 
<b>IDsAdminCreateObj</b> object with data about the container where the object will be created, the class of the object to be created and, possibly, the source object from which to copy.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/invoking-creation-wizards-from-your-application">Invoking Creation Wizards from Your Application</a>
 

 

