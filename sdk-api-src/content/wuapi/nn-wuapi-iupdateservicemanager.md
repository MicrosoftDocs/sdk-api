---
UID: NN:wuapi.IUpdateServiceManager
title: IUpdateServiceManager
author: windows-sdk-content
description: Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.
old-location: wua\iupdateservicemanager.htm
tech.root: Wua_Sdk
ms.assetid: 99b451b8-9831-475c-a4b0-7809f78d91b8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IUpdateServiceManager, IUpdateServiceManager interface [Windows Update Agent], IUpdateServiceManager interface [Windows Update Agent],described, wua.iupdateservicemanager, wuapi/IUpdateServiceManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateServiceManager interface


## -description


Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateServiceManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IUpdateServiceManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5b0677bb-9f19-4bb4-9942-8ca3da18b29a">AddScanPackageService</a>
</td>
<td align="left" width="63%">
Registers a scan package as a service with Windows Update Agent (WUA) and then returns an <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4071ef7-316f-4624-bc43-79c5982c4a82">AddService</a>
</td>
<td align="left" width="63%">
Registers a service with WUA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea54d96a-9ffb-4abd-a032-4dfcc7ba6403">RegisterServiceWithAU</a>
</td>
<td align="left" width="63%">
Registers a service with Automatic Updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fedd0979-1cc1-40c7-93d1-ade2f069ee76">RemoveService</a>
</td>
<td align="left" width="63%">
Removes a service registration from WUA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbf0b70c-5be0-4acc-9c44-bf32f6f752fd">SetOption</a>
</td>
<td align="left" width="63%">
Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d537594c-ccf3-463b-9860-612c5ea351cb">UnregisterServiceWithAU</a>
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

<a href="https://msdn.microsoft.com/9810e56b-a884-454b-adc8-ad839269dae3">Services</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/ae742fe2-c9f3-4116-b98a-3cf3906cfda2">IUpdateServiceCollection</a> of the services that are registered with WUA.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the UpdateServiceManager coclass. Use the Microsoft.Update.ServiceManager program identifier to create the object.



