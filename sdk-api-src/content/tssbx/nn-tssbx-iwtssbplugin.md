---
UID: NN:tssbx.IWTSSBPlugin
title: IWTSSBPlugin (tssbx.h)
description: Used to extend the capabilities of Terminal Services Session Broker (TS&#160;Session Broker). Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS&#160;Session Broker.
old-location: termserv\iwtssbplugin.htm
tech.root: TermServ
ms.assetid: f6959b8c-a8a8-438b-8b6d-31bf0e782bac
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin, IWTSSBPlugin interface [Remote Desktop Services], IWTSSBPlugin interface [Remote Desktop Services],described, termserv.iwtssbplugin, tssbx/IWTSSBPlugin
ms.topic: interface
f1_keywords:
- tssbx/IWTSSBPlugin
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSSBPlugin interface


## -description


<p class="CCE_Message">[The <b>IWTSSBPlugin</b> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).  Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSSBPlugin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSSBPlugin</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the plug-in and returns a value that indicates the redirection capabilities of the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-terminated">Terminated</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that TS Session Broker is about to destroy the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getmostsuitableserver">WTSSBX_GetMostSuitableServer</a>
</td>
<td align="left" width="63%">
Returns the ID of the server to which TS Session Broker should direct the incoming connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getuserexternalsession">WTSSBX_GetUserExternalSession</a>
</td>
<td align="left" width="63%">
Directs an incoming connection to an external computing resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_machinechangenotification">WTSSBX_MachineChangeNotification</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that a change occurred in the server environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_sessionchangenotification">WTSSBX_SessionChangeNotification</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that a change, such as a logon, logoff, disconnect, or reconnect, occurred in a user session.

</td>
</tr>
</table> 


## -remarks



TS Session Broker calls the <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getuserexternalsession">WTSSBX_GetUserExternalSession</a> method so that the plug-in can direct an incoming connection to a computer that does not belong to a farm in TS Session Broker.

Alternatively, TS Session Broker calls the <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getmostsuitableserver">WTSSBX_GetMostSuitableServer</a> method so that the plug-in can direct an incoming connection to a computer that does belong to a farm in TS Session Broker.

These methods reference an individual server in the farm by using the unique <i>MachineId</i> assigned to the server by TS Session Broker. When a server joins a farm in TS Session Broker, TS Session Broker calls the <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_machinechangenotification">WTSSBX_MachineChangeNotification</a> method to notify the plug-in of the change and pass the <i>MachineId</i> of the new server to the plug-in.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/extending-ts-session-broker">Remote Desktop Connection Broker Extensibility</a>
 

 

