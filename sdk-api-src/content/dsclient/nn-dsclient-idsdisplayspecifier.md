---
UID: NN:dsclient.IDsDisplaySpecifier
title: IDsDisplaySpecifier (dsclient.h)
description: Provides access to Active Directory Domain Service objects of the displaySpecifier class.
helpviewer_keywords: ["IDsDisplaySpecifier","IDsDisplaySpecifier interface [Active Directory]","IDsDisplaySpecifier interface [Active Directory]","described","_glines_idsdisplayspecifier","ad.idsdisplayspecifier","dsclient/IDsDisplaySpecifier"]
old-location: ad\idsdisplayspecifier.htm
tech.root: ad
ms.assetid: a6ac7006-73b8-4673-89d6-8285453481d3
ms.date: 12/05/2018
ms.keywords: IDsDisplaySpecifier, IDsDisplaySpecifier interface [Active Directory], IDsDisplaySpecifier interface [Active Directory],described, _glines_idsdisplayspecifier, ad.idsdisplayspecifier, dsclient/IDsDisplaySpecifier
req.header: dsclient.h
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
req.dll: Dsadmin.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsDisplaySpecifier
 - dsclient/IDsDisplaySpecifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier
---

# IDsDisplaySpecifier interface


## -description

The <b>IDsDisplaySpecifier</b> interface provides access to Active Directory Domain Service objects of the <b>displaySpecifier</b> class. Such objects are known as <i>display specifiers</i>. A display specifier stores data about how user interface elements, such as property pages or context menus, of an object in Active Directory Domain Services are to be displayed. For more information, see 
<a href="/windows/desktop/AD/display-specifiers">Display Specifiers</a>.

This interface is used to extend the display features of an existing object in Active Directory Domain Services, manage the display for a new directory object, or enhance the display of an Active Directory Domain Services enabled application. For more information, see 
<a href="/windows/desktop/AD/extending-the-user-interface-for-directory-objects">Extending the User Interface for Directory Objects</a>.

To create an instance of this interface,  call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsDisplaySpecifier</b> object identifier as shown in the following code  example.

```cpp
#include <objbase.h>
#define INITGUID
#include <initguid.h>
#include "dsclient.h"
 
HRESULT hr;
IDsDisplaySpecifier *pDS;

CoInitialize(NULL);

hr = CoCreateInstance( CLSID_DsDisplaySpecifier,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_IDsDisplaySpecifier,
                       (void**)&pDS);
if(SUCCEEDED(hr))
{
    // More code calling the interface methods.
    
    pDS->Release();
}
 
CoUninitialize();
```

## -inheritance

The <b>IDsDisplaySpecifier</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsDisplaySpecifier</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-icommonquery">ICommonQuery</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-iqueryform">IQueryForm</a>
