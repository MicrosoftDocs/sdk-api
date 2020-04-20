---
UID: NN:wuapi.IUpdateServiceManager
title: IUpdateServiceManager (wuapi.h)
description: Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.helpviewer_keywords: ["IUpdateServiceManager","IUpdateServiceManager interface [Windows Update Agent]","IUpdateServiceManager interface [Windows Update Agent]","described","wua.iupdateservicemanager","wuapi/IUpdateServiceManager"]
old-location: wua\iupdateservicemanager.htm
tech.root: Wua_Sdk
ms.assetid: 99b451b8-9831-475c-a4b0-7809f78d91b8
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager, IUpdateServiceManager interface [Windows Update Agent], IUpdateServiceManager interface [Windows Update Agent],described, wua.iupdateservicemanager, wuapi/IUpdateServiceManager
f1_keywords:
- wuapi/IUpdateServiceManager
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
- IUpdateServiceManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateServiceManager interface


## -description


Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateServiceManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateServiceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdateServiceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice">AddScanPackageService</a>
</td>
<td align="left" width="63%">
Registers a scan package as a service with Windows Update Agent (WUA) and then returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateservice">IUpdateService</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-addservice">AddService</a>
</td>
<td align="left" width="63%">
Registers a service with WUA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau">RegisterServiceWithAU</a>
</td>
<td align="left" width="63%">
Registers a service with Automatic Updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-removeservice">RemoveService</a>
</td>
<td align="left" width="63%">
Removes a service registration from WUA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-setoption">SetOption</a>
</td>
<td align="left" width="63%">
Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau">UnregisterServiceWithAU</a>
</td>
<td align="left" width="63%">
Unregisters a service with Automatic Updates.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateServiceManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-get_services">Services</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateservicecollection">IUpdateServiceCollection</a> of the services that are registered with WUA.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the UpdateServiceManager coclass. Use the Microsoft.Update.ServiceManager program identifier to create the object.



