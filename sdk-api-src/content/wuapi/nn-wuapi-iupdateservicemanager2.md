---
UID: NN:wuapi.IUpdateServiceManager2
title: IUpdateServiceManager2 (wuapi.h)
description: Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.
old-location: wua\iupdateservicemanager2.htm
tech.root: Wua_Sdk
ms.assetid: 26b75edc-eb43-4ee0-8040-da8b3252cf21
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager2, IUpdateServiceManager2 interface [Windows Update Agent], IUpdateServiceManager2 interface [Windows Update Agent],described, wua.iupdateservicemanager2, wuapi/IUpdateServiceManager2
ms.topic: interface
f1_keywords:
- wuapi/IUpdateServiceManager2
dev_langs:
- c++
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- IUpdateServiceManager2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateServiceManager2 interface


## -description


 Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateServiceManager2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>. <b>IUpdateServiceManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdateServiceManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager2-addservice2">AddService2</a>
</td>
<td align="left" width="63%">
Registers a service with WUA without requiring an authorization cabinet file (.cab), and returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateservicecollection">IUpdateServiceRegistration</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager2-queryserviceregistration">QueryServiceRegistration</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateserviceregistration">IUpdateServiceRegistration</a> interface.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateServiceManager2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager2-get_clientapplicationid">ClientApplicationID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the identifier of the current client application.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the UpdateServiceManager coclass. Use the Microsoft.Update.ServiceManager program identifier to create the object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>
 

 

