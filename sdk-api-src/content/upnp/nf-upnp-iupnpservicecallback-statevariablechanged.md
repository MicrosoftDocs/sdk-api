---
UID: NF:upnp.IUPnPServiceCallback.StateVariableChanged
title: IUPnPServiceCallback::StateVariableChanged (upnp.h)
author: windows-sdk-content
description: The StateVariableChanged method is invoked when a state variable has changed.
old-location: upnp\iupnpservicecallback_statevariablechanged.htm
tech.root: upnp
ms.assetid: 68dac38e-535b-491e-a9a5-0f6bccb7fcc1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUPnPServiceCallback interface [UPnP APIs],StateVariableChanged method, IUPnPServiceCallback.StateVariableChanged, IUPnPServiceCallback::StateVariableChanged, StateVariableChanged, StateVariableChanged method [UPnP APIs], StateVariableChanged method [UPnP APIs],IUPnPServiceCallback interface, _upnp_iupnpservicecallback_statevariablechanged, upnp.iupnpservicecallback_statevariablechanged, upnp/IUPnPServiceCallback::StateVariableChanged
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceCallback.StateVariableChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPServiceCallback::StateVariableChanged


## -description


The 
<b>StateVariableChanged</b> method is invoked when a state variable has changed.


## -parameters




### -param pus [in]

Reference to an 
<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a> object that specifies the service about which the UPnP framework is sending the notification.


### -param pcwszStateVarName [in]

Reference to a string that specifies the name of the state variable that has changed.


### -param vaValue [in]

Specifies the new value. The type of the data returned depends on the data type of the state variable for which the notification is sent.


## -returns



The application should return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a>



<a href="https://msdn.microsoft.com/f5797907-ae65-48e6-adf8-b717bfb5101f">IUPnPService::AddCallback</a>



<a href="https://msdn.microsoft.com/44515be4-891b-4f3d-a2c2-1699e468e708">IUPnPServiceCallback</a>
 

 

