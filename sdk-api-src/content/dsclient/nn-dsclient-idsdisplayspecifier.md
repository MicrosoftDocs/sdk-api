---
UID: NN:dsclient.IDsDisplaySpecifier
title: IDsDisplaySpecifier
author: windows-sdk-content
description: Provides access to Active Directory Domain Service objects of the displaySpecifier class.
old-location: ad\idsdisplayspecifier.htm
tech.root: ad
ms.assetid: a6ac7006-73b8-4673-89d6-8285453481d3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDsDisplaySpecifier, IDsDisplaySpecifier interface [Active Directory], IDsDisplaySpecifier interface [Active Directory],described, _glines_idsdisplayspecifier, ad.idsdisplayspecifier, dsclient/IDsDisplaySpecifier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsDisplaySpecifier interface


## -description


The <b>IDsDisplaySpecifier</b> interface provides access to Active Directory Domain Service objects of the <b>displaySpecifier</b> class. Such objects are known as <i>display specifiers</i>. A display specifier stores data about how user interface elements, such as property pages or context menus, of an object in Active Directory Domain Services are to be displayed. For more information, see 
<a href="https://msdn.microsoft.com/0c31b02b-9fd3-4547-9ebc-d511a10d7106">Display Specifiers</a>.

This interface is used to extend the display features of an existing object in Active Directory Domain Services, manage the display for a new directory object, or enhance the display of an Active Directory Domain Services enabled application. For more information, see 
<a href="https://msdn.microsoft.com/758ec25d-42ab-46ba-aa58-416d7ac8fd68">Extending the User Interface for Directory Objects</a>.

To create an instance of this interface,  call <a href="_com_cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsDisplaySpecifier</b> object identifier as shown in the following code  example.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;objbase.h&gt;
#define INITGUID
#include &lt;initguid.h&gt;
#include "dsclient.h"
 
HRESULT hr;
IDsDisplaySpecifier *pDS;

CoInitialize(NULL);

hr = CoCreateInstance( CLSID_DsDisplaySpecifier,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_IDsDisplaySpecifier,
                       (void**)&amp;pDS);
if(SUCCEEDED(hr))
{
    // More code calling the interface methods.
    
    pDS-&gt;Release();
}
 
CoUninitialize();</pre>
</td>
</tr>
</table></span></div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsDisplaySpecifier</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsDisplaySpecifier</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/78b8e280-454c-4db7-9037-ea7e42798323">EnumClassAttributes</a>
</td>
<td align="left" width="63%">
Enumerates the attributes for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e9ecbee-b298-42a4-ad02-28bab9d99b6b">GetAttributeADsType</a>
</td>
<td align="left" width="63%">
Obtains the attribute type for a given attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23b88707-c4c3-47dd-a5bc-e325142602f5">GetClassCreationInfo</a>
</td>
<td align="left" width="63%">
Obtains data about the class creation wizard objects for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4fc25f6-0157-406d-b523-8542183291ed">GetDisplaySpecifier</a>
</td>
<td align="left" width="63%">
Binds to the display specifier object for a given class in Active Directory Domain Services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a4551ec-0b73-4119-8fdd-1e1952f60bd2">GetFriendlyAttributeName</a>
</td>
<td align="left" width="63%">
Obtains the localized name of an attribute of a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/192e2a57-6bde-4357-893e-37f466588b55">GetFriendlyClassName</a>
</td>
<td align="left" width="63%">
Obtains the localized name for an object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7057779b-4176-41a3-bc7e-0d6958baf245">GetIcon</a>
</td>
<td align="left" width="63%">
Obtains the icon for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5e65bde-aa2d-47e0-8cfc-062b14da3e87">GetIconLocation</a>
</td>
<td align="left" width="63%">
Obtains the icon location for a given object class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1717200a-353b-413e-97a2-0742a95056d8">IsClassContainer</a>
</td>
<td align="left" width="63%">
Determines if a given object class is a container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/306538a4-dccc-4f4f-89fa-491d08718d14">SetLanguageID</a>
</td>
<td align="left" width="63%">
Changes the locale used by the  <b>IDsDisplaySpecifier</b> object to a specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f72cc711-7dec-4f5a-9cf1-57612240b435">SetServer</a>
</td>
<td align="left" width="63%">
Specifies the server from which display specifier data is obtained.

</td>
</tr>
</table> 


## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/56d05afb-6e5e-41be-bc10-61192c1c1312">ICommonQuery</a>



<a href="https://msdn.microsoft.com/f50caa34-d29e-4ad1-98b0-ef5c1f5550bf">IDsBrowseDomainTree</a>



<a href="https://msdn.microsoft.com/9d90f119-3d10-4f06-bed4-5ffab9ae14a4">IPersistQuery</a>



<a href="https://msdn.microsoft.com/fd4f41f0-8aeb-4c83-a079-a5a77685c143">IQueryForm</a>
 

 

