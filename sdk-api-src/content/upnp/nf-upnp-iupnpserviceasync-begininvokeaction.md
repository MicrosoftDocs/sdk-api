---
UID: NF:upnp.IUPnPServiceAsync.BeginInvokeAction
title: IUPnPServiceAsync::BeginInvokeAction
author: windows-sdk-content
description: BeginInvokeAction method invokes an action on a device in asynchronous mode. Additionally, if a delayed SCPD download and event subscription is opted-in, and it has not taken place already, this method will initiate SCPD download.
old-location: upnp\iupnpserviceasync_begininvokeaction.htm
old-project: upnp
ms.assetid: 40900CE1-03EE-451A-84DE-5C496EB2D7E5
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: BeginInvokeAction, BeginInvokeAction method [UPnP APIs], BeginInvokeAction method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],BeginInvokeAction method, IUPnPServiceAsync.BeginInvokeAction, IUPnPServiceAsync::BeginInvokeAction, upnp.iupnpserviceasync_begininvokeaction, upnp/IUPnPServiceAsync::BeginInvokeAction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync.BeginInvokeAction
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceAsync::BeginInvokeAction


## -description


The 	<b>BeginInvokeAction</b> method invokes an action on a device in asynchronous mode. Additionally, if a delayed SCPD download and event subscription is opted-in, and it has not taken place already, this method will initiate SCPD download. 


## -parameters




### -param bstrActionName [in]

Specifies the method to invoke.


### -param vInActionArgs [in]

Specifies an array of input arguments to the method. If the action has no input arguments, this parameter must contain an empty array.  The contents of this array are service-specific.


### -param pAsyncResult [in, optional]

Pointer  to a <a href="https://msdn.microsoft.com/53854510-BB0C-41E6-8651-F34991B24D5E">IUPnPAsyncResult</a> object. When the <b>BeginInvokeAction</b> call is complete, 
	UPnP will use the <a href="https://msdn.microsoft.com/C71C0A78-C3D1-4725-99E2-542786B03C8F">IUPnPAsyncResult::AsyncOperationComplete</a> method to notify the control 
	point.



### -param pullRequestID [out]

Pointer to a 64-bit <b>ULONG</b> value used to identify the asynchronous I/O operation. The control point must use this handle as a cookie while ending or cancelling this  operation with <a href="https://msdn.microsoft.com/1B10F8E9-D3C9-432B-B773-77B4BB82224C">EndInvokeAction</a>.


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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Another async operation is being done on this <a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a> object. Create another <b>IUPnPServiceAsync</b> instance or cancel the running operation by using <a href="https://msdn.microsoft.com/FBEC2DF3-6D45-49F2-AAA8-6DED697BC5A6">IUPnPServiceAsync::CancelAsyncOperation</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to initiate the  operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_ACTION</b></dt>
</dl>
</td>
<td width="60%">
This action is not supported by the device.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/1B10F8E9-D3C9-432B-B773-77B4BB82224C">IUPnPServiceAsync::EndInvokeAction</a>
 

 

