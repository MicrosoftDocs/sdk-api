---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDsAdminCreateObj interface


## -description


The <b>IDsAdminCreateObj</b> interface is implemented by the system and used by an application or component to programmatically start a creation wizard for a specified object class.

To obtain an instance of this interface, call <a href="_com_cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsAdminCreateObj</b> class identifier as shown below.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;initguid.h&gt;
#include &lt;dsadmin.h&gt;

HRESULT hr = S_OK;
IDsAdminCreateObj* pCreateObj = NULL;
hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
        NULL, CLSCTX_INPROC_SERVER,
        IID_IDsAdminCreateObj,
        (void**)&amp;pCreateObj);</pre>
</td>
</tr>
</table></span></div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminCreateObj</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsAdminCreateObj</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8c157dd8-b569-4171-bd23-b9bce80dbc21">CreateModal</a>
</td>
<td align="left" width="63%">
Displays the creation wizard and returns the newly created object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the 
<b>IDsAdminCreateObj</b> object with data about the container where the object will be created, the class of the object to be created and, possibly, the source object from which to copy.

</td>
</tr>
</table> 


## -see-also




<a href="ad.admin_interfaes_in_active_directory_domain_services">Admin Interfaces in Active Directory Domain Services</a>



<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/be4b6101-f795-403b-b93e-960759ac4f14">Invoking Creation Wizards from Your Application</a>
 

 

