---
UID: NN:dsclient.IDsDisplaySpecifier
title: IDsDisplaySpecifier (dsclient.h)
description: Provides access to Active Directory Domain Service objects of the displaySpecifier class.
old-location: ad\idsdisplayspecifier.htm
tech.root: ad
ms.assetid: a6ac7006-73b8-4673-89d6-8285453481d3
ms.date: 12/05/2018
ms.keywords: IDsDisplaySpecifier, IDsDisplaySpecifier interface [Active Directory], IDsDisplaySpecifier interface [Active Directory],described, _glines_idsdisplayspecifier, ad.idsdisplayspecifier, dsclient/IDsDisplaySpecifier
f1_keywords:
- dsclient/IDsDisplaySpecifier
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dsadmin.dll
api_name:
- IDsDisplaySpecifier
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsDisplaySpecifier interface


## -description


The <b>IDsDisplaySpecifier</b> interface provides access to Active Directory Domain Service objects of the <b>displaySpecifier</b> class. Such objects are known as <i>display specifiers</i>. A display specifier stores data about how user interface elements, such as property pages or context menus, of an object in Active Directory Domain Services are to be displayed. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/AD/display-specifiers">Display Specifiers</a>.

This interface is used to extend the display features of an existing object in Active Directory Domain Services, manage the display for a new directory object, or enhance the display of an Active Directory Domain Services enabled application. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/AD/extending-the-user-interface-for-directory-objects">Extending the User Interface for Directory Objects</a>.

To create an instance of this interface,  call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsDisplaySpecifier</b> object identifier as shown in the following code  example.

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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsDisplaySpecifier</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsDisplaySpecifier</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsDisplaySpecifier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-enumclassattributes">EnumClassAttributes</a>
</td>
<td align="left" width="63%">
Enumerates the attributes for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getattributeadstype">GetAttributeADsType</a>
</td>
<td align="left" width="63%">
Obtains the attribute type for a given attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getclasscreationinfo">GetClassCreationInfo</a>
</td>
<td align="left" width="63%">
Obtains data about the class creation wizard objects for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getdisplayspecifier">GetDisplaySpecifier</a>
</td>
<td align="left" width="63%">
Binds to the display specifier object for a given class in Active Directory Domain Services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getfriendlyattributename">GetFriendlyAttributeName</a>
</td>
<td align="left" width="63%">
Obtains the localized name of an attribute of a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getfriendlyclassname">GetFriendlyClassName</a>
</td>
<td align="left" width="63%">
Obtains the localized name for an object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-geticon">GetIcon</a>
</td>
<td align="left" width="63%">
Obtains the icon for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-geticonlocation">GetIconLocation</a>
</td>
<td align="left" width="63%">
Obtains the icon location for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-isclasscontainer">IsClassContainer</a>
</td>
<td align="left" width="63%">
Determines if a given object class is a container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-setlanguageid">SetLanguageID</a>
</td>
<td align="left" width="63%">
Changes the locale used by the  <b>IDsDisplaySpecifier</b> object to a specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-setserver">SetServer</a>
</td>
<td align="left" width="63%">
Specifies the server from which display specifier data is obtained.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nn-cmnquery-icommonquery">ICommonQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nn-cmnquery-iqueryform">IQueryForm</a>
 

 

