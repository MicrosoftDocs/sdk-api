---
UID: NF:tapi3if.ITTAPI.RegisterCallNotifications
title: ITTAPI::RegisterCallNotifications
author: windows-sdk-content
description: The RegisterCallNotifications method sets which new call notifications an application will receive. The application must call the method for each address, indicating media type or types it can handle, and specifying the privileges it requests.
old-location: tapi3\ittapi_registercallnotifications.htm
old-project: Tapi
ms.assetid: 335deb2c-7700-4101-b6fa-f7fe0f248307
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITTAPI interface [TAPI 2.2],RegisterCallNotifications method, ITTAPI.RegisterCallNotifications, ITTAPI::RegisterCallNotifications, RegisterCallNotifications, RegisterCallNotifications method [TAPI 2.2], RegisterCallNotifications method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_registercallnotifications, tapi3.ittapi_registercallnotifications, tapi3if/ITTAPI::RegisterCallNotifications
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI.RegisterCallNotifications
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPI::RegisterCallNotifications


## -description


The 
<b>RegisterCallNotifications</b> method sets which new call notifications an application will receive. The application must call the method for each address, indicating media type or types it can handle, and specifying the privileges it requests.

An application that will make only outgoing calls does not need to call this method.

The 
<a href="https://msdn.microsoft.com/06cfe56c-907f-49ed-8a7a-db31383a06f9">ITTAPIEventNotification</a> outgoing interface must be registered prior to calling this method.

If both owner and monitor privileges are needed for an address, this method should be called only once, with both <i>fMonitor</i> and <i>fOwner</i> set to <b>TRUE</b>.


## -parameters




### -param pAddress [in]

Pointer to 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface.


### -param fMonitor [in]

Boolean value indicating whether the application will monitor calls. VARIANT_TRUE indicates that the application will monitor calls; VARIANT_FALSE that it will not.


### -param fOwner [in]

Boolean value indicating whether the application will own incoming calls. VARIANT_TRUE indicates that the application will own incoming calls; VARIANT_FALSE indicates that it will not.


### -param lMediaTypes [in]


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media types</a> that can be handled by the application.


### -param lCallbackInstance [in]

Callback instance to be used by the TAPI 3 DLL. Can be the gulAdvise value returned by <a href="https://msdn.microsoft.com/en-us/library/ms678815(v=VS.85).aspx">IConnectionPoint::Advise</a> during registration of the 
<a href="https://msdn.microsoft.com/06cfe56c-907f-49ed-8a7a-db31383a06f9">ITTAPIEventNotification</a> outgoing interface.


### -param plRegister [out]

On success, the returned value that is used by 
<a href="https://msdn.microsoft.com/66717165-1c29-4d77-b6ac-8c3638fb11f4">ITTAPI::UnregisterNotifications</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plRegister</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The TAPI object has not been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



If multiple calls of this method are used on one address, the information about participant calls from a call hub may be confusing if a call that is already being monitored by the application is handed off to it.

The <b>RegisterCallNotifications</b> method registers the application as having an interest in monitoring calls or receiving ownership of calls that are of the specified media types. These call privileges are set in the <i>fMonitor</i> and <i>fOwner</i> parameters. 
An application can specify multiple flags to handle multiple media types. Conflicts can arise if multiple applications register for the same address and media type. These conflicts are resolved by a priority scheme in which the user assigns relative priorities to the applications. Users can set application priorities by calling the <a href="https://msdn.microsoft.com/ca049695-02d0-4b30-ad1f-60cdbf0a4dbd">ITTAPI::SetApplicationPriority</a> function. Only the highest priority application for a given media type will receive ownership (unsolicited) of a call of that media type. Ownership can be received when an incoming call first arrives or when a call is handed off. The <a href="https://msdn.microsoft.com/a96a3790-ee5d-4983-b69a-30c7af96afd9">ITBasicCallControl::HandoffDirect</a> and  <a href="https://msdn.microsoft.com/02579638-fafd-4c4a-91a3-460d7ebf6917">ITBasicCallControl::HandoffIndirect</a> functions are called  to hand off ownership of a call to another application. If the user does not assign priorities to the application, and multiple applications open the same line device, by default, the application that called <b>RegisterCallNotifications</b> first will have the highest priority. 





## -see-also




<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events overview</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>



<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/06cfe56c-907f-49ed-8a7a-db31383a06f9">ITTAPIEventNotification</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

