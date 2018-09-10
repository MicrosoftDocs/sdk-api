---
UID: NN:tssbx.IWTSSBPlugin
title: IWTSSBPlugin
author: windows-sdk-content
description: Used to extend the capabilities of Terminal Services Session Broker (TS&#160;Session Broker). Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS&#160;Session Broker.
old-location: termserv\iwtssbplugin.htm
tech.root: termserv
ms.assetid: f6959b8c-a8a8-438b-8b6d-31bf0e782bac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWTSSBPlugin, IWTSSBPlugin interface [Remote Desktop Services], IWTSSBPlugin interface [Remote Desktop Services],described, termserv.iwtssbplugin, tssbx/IWTSSBPlugin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tssbx.h
api_name:
 - IWTSSBPlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSSBPlugin interface


## -description


<p class="CCE_Message">[The <b>IWTSSBPlugin</b> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a> interface.]

Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).  Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSSBPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSSBPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSSBPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9304f4a-49ed-4a5e-87a1-7a9bc1c01b3d">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the plug-in and returns a value that indicates the redirection capabilities of the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/123455dd-6ef3-409f-b021-e641868b16f0">Terminated</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that TS Session Broker is about to destroy the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d25527ec-1007-4b7b-93ad-6c96780dddec">WTSSBX_GetMostSuitableServer</a>
</td>
<td align="left" width="63%">
Returns the ID of the server to which TS Session Broker should direct the incoming connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/989cd7bc-932f-4a33-91c8-e66fac7195ad">WTSSBX_GetUserExternalSession</a>
</td>
<td align="left" width="63%">
Directs an incoming connection to an external computing resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/226ca68e-6c3d-4160-a569-ca0b92cb9316">WTSSBX_MachineChangeNotification</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that a change occurred in the server environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00426aa2-1d22-462f-9ad1-2a63d151493d">WTSSBX_SessionChangeNotification</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that a change, such as a logon, logoff, disconnect, or reconnect, occurred in a user session.

</td>
</tr>
</table> 


## -remarks



TS Session Broker calls the <a href="https://msdn.microsoft.com/989cd7bc-932f-4a33-91c8-e66fac7195ad">WTSSBX_GetUserExternalSession</a> method so that the plug-in can direct an incoming connection to a computer that does not belong to a farm in TS Session Broker.

Alternatively, TS Session Broker calls the <a href="https://msdn.microsoft.com/d25527ec-1007-4b7b-93ad-6c96780dddec">WTSSBX_GetMostSuitableServer</a> method so that the plug-in can direct an incoming connection to a computer that does belong to a farm in TS Session Broker.

These methods reference an individual server in the farm by using the unique <i>MachineId</i> assigned to the server by TS Session Broker. When a server joins a farm in TS Session Broker, TS Session Broker calls the <a href="https://msdn.microsoft.com/226ca68e-6c3d-4160-a569-ca0b92cb9316">WTSSBX_MachineChangeNotification</a> method to notify the plug-in of the change and pass the <i>MachineId</i> of the new server to the plug-in.




## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/f111d6e6-90ca-4eff-ab0e-02de25f7d6ad">Remote Desktop Connection Broker Extensibility</a>
 

 

