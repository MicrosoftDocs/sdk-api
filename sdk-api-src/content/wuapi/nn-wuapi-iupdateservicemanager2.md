---
UID: NN:wuapi.IUpdateServiceManager2
title: IUpdateServiceManager2
author: windows-sdk-content
description: Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.
old-location: wua\iupdateservicemanager2.htm
old-project: wua_sdk
ms.assetid: 26b75edc-eb43-4ee0-8040-da8b3252cf21
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUpdateServiceManager2, IUpdateServiceManager2 interface [Windows Update Agent], IUpdateServiceManager2 interface [Windows Update Agent],described, wua.iupdateservicemanager2, wuapi/IUpdateServiceManager2
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceManager2
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateServiceManager2 interface


## -description


 Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateServiceManager2</b> interface inherits from <a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>. <b>IUpdateServiceManager2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1584b92f-ba21-4b03-a1b4-540313eb7893">AddService2</a>
</td>
<td align="left" width="63%">
Registers a service with WUA without requiring an authorization cabinet file (.cab), and returns a pointer to an <a href="https://msdn.microsoft.com/ae742fe2-c9f3-4116-b98a-3cf3906cfda2">IUpdateServiceRegistration</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8fd077f-f4a9-4db0-8a47-14241bc574fb">QueryServiceRegistration</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://msdn.microsoft.com/729664f2-5f75-4e73-9ccc-150b2e201f66">IUpdateServiceRegistration</a> interface.

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

<a href="https://msdn.microsoft.com/6783b7fc-ebb7-4b68-b71c-23e65ef61504">ClientApplicationID</a>


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




<a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>
 

 

