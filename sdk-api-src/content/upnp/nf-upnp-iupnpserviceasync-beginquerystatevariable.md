---
UID: NF:upnp.IUPnPServiceAsync.BeginQueryStateVariable
title: IUPnPServiceAsync::BeginQueryStateVariable
author: windows-sdk-content
description: BeginQueryStateVariable method initiates an asynchronous request for the state variable value from a specific service.
old-location: upnp\iupnpserviceasync_beginquerystatevariable.htm
tech.root: UPnP
ms.assetid: 1E97589C-A06B-4012-A2A2-C88BBE9B2530
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: BeginQueryStateVariable, BeginQueryStateVariable method [UPnP APIs], BeginQueryStateVariable method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],BeginQueryStateVariable method, IUPnPServiceAsync.BeginQueryStateVariable, IUPnPServiceAsync::BeginQueryStateVariable, upnp.iupnpserviceasync_beginquerystatevariable, upnp/IUPnPServiceAsync::BeginQueryStateVariable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUPnPServiceAsync.BeginQueryStateVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- upnp.h
: 
- IUPnPServiceAsync.BeginQueryStateVariable
: 
---

# IUPnPServiceAsync::BeginQueryStateVariable


## -description


The <b>BeginQueryStateVariable</b> method initiates an asynchronous request for the state variable value from a specific service. Additionally, if opt-in is indicated for a delayed Service Control Protocol Description (SCPD) download and event subscription, and it has not taken place already, this method will initiate SCPD download and event subscription. 


## -parameters




### -param bstrVariableName [in]

Specifies the requested state variable value.


### -param pAsyncResult [in, optional]

Pointer  to a <a href="https://msdn.microsoft.com/53854510-BB0C-41E6-8651-F34991B24D5E">IUPnPAsyncResult</a> object. When the <b>BeginQueryStateVariable</b> call is complete, 
	UPnP will use the <a href="https://msdn.microsoft.com/C71C0A78-C3D1-4725-99E2-542786B03C8F">IUPnPAsyncResult::AsyncOperationComplete</a> method to notify the control 
	point.



### -param pullRequestID [out]

Pointer to a 64-bit <b>ULONG</b> value used to identify the asynchronous I/O operation. The UPnP control point must use this handle when ending or cancelling this  operation with <a href="https://msdn.microsoft.com/82AAB2C4-46A9-4545-95E1-887841735815">EndQueryStateVariable</a>.


## -returns



Returns <b>S_OK</b> on success. Otherwise, the method returns a COM error code defined in <b>WinError.h</b> or one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to initiate the asynchronous operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_VARIABLE</b></dt>
</dl>
</td>
<td width="60%">
The requested state variable, indicated by <i>bstrVariableName</i>, does not exist.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.</div>
<div> </div>



## -remarks



Event subscription should be completed before querying any evented state variables with this method. If this does not occur,  <b>UPNP_E_VARIABLE_VALUE_UNKNOWN</b> is returned, and  event subscription will take place internally. As a result, the next <b>BeginQueryStateVariable</b> call will succeed.

<div class="alert"><b>Note</b>  For services without evented variables, this method will always behave as expected.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/FBEC2DF3-6D45-49F2-AAA8-6DED697BC5A6">IUPnPServiceAsync::CancelAsyncOperation</a>
 

 

