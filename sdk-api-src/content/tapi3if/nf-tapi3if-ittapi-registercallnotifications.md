---
UID: NF:tapi3if.ITTAPI.RegisterCallNotifications
title: ITTAPI::RegisterCallNotifications (tapi3if.h)
description: The RegisterCallNotifications method sets which new call notifications an application will receive. The application must call the method for each address, indicating media type or types it can handle, and specifying the privileges it requests.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","RegisterCallNotifications method","ITTAPI.RegisterCallNotifications","ITTAPI::RegisterCallNotifications","RegisterCallNotifications","RegisterCallNotifications method [TAPI 2.2]","RegisterCallNotifications method [TAPI 2.2]","ITTAPI interface","_tapi3_ittapi_registercallnotifications","tapi3.ittapi_registercallnotifications","tapi3if/ITTAPI::RegisterCallNotifications"]
old-location: tapi3\ittapi_registercallnotifications.htm
tech.root: tapi3
ms.assetid: 335deb2c-7700-4101-b6fa-f7fe0f248307
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],RegisterCallNotifications method, ITTAPI.RegisterCallNotifications, ITTAPI::RegisterCallNotifications, RegisterCallNotifications, RegisterCallNotifications method [TAPI 2.2], RegisterCallNotifications method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_registercallnotifications, tapi3.ittapi_registercallnotifications, tapi3if/ITTAPI::RegisterCallNotifications
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTAPI::RegisterCallNotifications
 - tapi3if/ITTAPI::RegisterCallNotifications
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI.RegisterCallNotifications
---

# ITTAPI::RegisterCallNotifications


## -description

The 
<b>RegisterCallNotifications</b> method sets which new call notifications an application will receive. The application must call the method for each address, indicating media type or types it can handle, and specifying the privileges it requests.

An application that will make only outgoing calls does not need to call this method.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a> outgoing interface must be registered prior to calling this method.

If both owner and monitor privileges are needed for an address, this method should be called only once, with both <i>fMonitor</i> and <i>fOwner</i> set to <b>TRUE</b>.

## -parameters

### -param pAddress [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface.

### -param fMonitor [in]

Boolean value indicating whether the application will monitor calls. VARIANT_TRUE indicates that the application will monitor calls; VARIANT_FALSE that it will not.

### -param fOwner [in]

Boolean value indicating whether the application will own incoming calls. VARIANT_TRUE indicates that the application will own incoming calls; VARIANT_FALSE indicates that it will not.

### -param lMediaTypes [in]

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media types</a> that can be handled by the application.

### -param lCallbackInstance [in]

Callback instance to be used by the TAPI 3 DLL. Can be the gulAdvise value returned by <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">IConnectionPoint::Advise</a> during registration of the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a> outgoing interface.

### -param plRegister [out]

On success, the returned value that is used by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications">ITTAPI::UnregisterNotifications</a>.

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
An application can specify multiple flags to handle multiple media types. Conflicts can arise if multiple applications register for the same address and media type. These conflicts are resolved by a priority scheme in which the user assigns relative priorities to the applications. Users can set application priorities by calling the <a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-setapplicationpriority">ITTAPI::SetApplicationPriority</a> function. Only the highest priority application for a given media type will receive ownership (unsolicited) of a call of that media type. Ownership can be received when an incoming call first arrives or when a call is handed off. The <a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect">ITBasicCallControl::HandoffDirect</a> and  <a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect">ITBasicCallControl::HandoffIndirect</a> functions are called  to hand off ownership of a call to another application. If the user does not assign priorities to the application, and multiple applications open the same line device, by default, the application that called <b>RegisterCallNotifications</b> first will have the highest priority.

## -see-also

<a href="/windows/desktop/Tapi/events">Events overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>