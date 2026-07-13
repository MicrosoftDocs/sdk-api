---
UID: NF:wia_xp.IWiaDevMgr.RegisterEventCallbackCLSID
title: IWiaDevMgr::RegisterEventCallbackCLSID (wia_xp.h)
description: The IWiaDevMgr::RegisterEventCallbackCLSID method registers an application to receive events even if the application may not be running.
helpviewer_keywords: ["IWiaDevMgr interface [WIA]","RegisterEventCallbackCLSID method","IWiaDevMgr.RegisterEventCallbackCLSID","IWiaDevMgr::RegisterEventCallbackCLSID","RegisterEventCallbackCLSID","RegisterEventCallbackCLSID method [WIA]","RegisterEventCallbackCLSID method [WIA]","IWiaDevMgr interface","_wia_IWiaDevMgr_RegisterEventCallbackCLSID","wia._wia_IWiaDevMgr_RegisterEventCallbackCLSID","wia_xp/IWiaDevMgr::RegisterEventCallbackCLSID"]
old-location: wia\_wia_IWiaDevMgr_RegisterEventCallbackCLSID.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\registereventcallbackclsid.htm
ms.date: 12/05/2018
ms.keywords: IWiaDevMgr interface [WIA],RegisterEventCallbackCLSID method, IWiaDevMgr.RegisterEventCallbackCLSID, IWiaDevMgr::RegisterEventCallbackCLSID, RegisterEventCallbackCLSID, RegisterEventCallbackCLSID method [WIA], RegisterEventCallbackCLSID method [WIA],IWiaDevMgr interface, _wia_IWiaDevMgr_RegisterEventCallbackCLSID, wia._wia_IWiaDevMgr_RegisterEventCallbackCLSID, wia_xp/IWiaDevMgr::RegisterEventCallbackCLSID
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaDevMgr::RegisterEventCallbackCLSID
 - wia_xp/IWiaDevMgr::RegisterEventCallbackCLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDevMgr.RegisterEventCallbackCLSID
archived: true
---

# IWiaDevMgr::RegisterEventCallbackCLSID


## -description

The <b>IWiaDevMgr::RegisterEventCallbackCLSID</b> method registers an application to receive events even if the application may not be running.

## -parameters

### -param lFlags [in]

Type: <b>LONG</b>

Specifies registration flags. Can be set to the following values:



<table class="clsStd">
<tr>
<th>Registration Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>WIA_REGISTER_EVENT_CALLBACK</td>
<td>Register for the event.</td>
</tr>
<tr>
<td>WIA_UNREGISTER_EVENT_CALLBACK</td>
<td>Delete the registration for the event.</td>
</tr>
<tr>
<td>WIA_SET_DEFAULT_HANDLER</td>
<td>Set the application as the default event handler.</td>
</tr>
</table>

### -param bstrDeviceID [in]

Type: <b>BSTR</b>

Specifies a device identifier. Pass <b>NULL</b> to register for the event on all WIA devices.

### -param pEventGUID [in]

Type: <b>const GUID*</b>

Specifies the event for which the application is registering. For a list of standard events, see <a href="/windows/desktop/wia/-wia-wia-event-identifiers">WIA Event Identifiers</a>.

### -param pClsID [in]

Type: <b>const GUID*</b>

Pointer to the application's class ID (<b>CLSID</b>). The WIA run-time system uses the application's <b>CLSID</b> to start the application when an event occurs for which it is registered.

### -param bstrName [in]

Type: <b>BSTR</b>

Specifies the name of the application that registers for the event.

### -param bstrDescription [in]

Type: <b>BSTR</b>

Specifies a text description of the application that registers for the event.

### -param bstrIcon [in]

Type: <b>BSTR</b>

Specifies the name of an image file to be used for the icon for the application that registers for the event.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

WIA applications use this method to register to receive hardware device events of the type WIA_ACTION_EVENT. Once programs call <b>IWiaDevMgr::RegisterEventCallbackCLSID</b>, they are registered to receive WIA device events even if they are not running. 

When the event occurs, the WIA system determines which application is registered to receive the event. It uses the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function and the class ID specified in the <i>pClsID</i> parameter to create an instance of the application. It then calls the application's <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback">ImageEventCallback</a> method to transmit the event information.

An application can invoke the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo">EnumRegisterEventInfo</a> method to enumerate event registration information.

An application can find whether an event is an action type or notification type (or both) event by examining the <b>ulFlags</b> value of a <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_dev_cap">WIA_DEV_CAP</a> structure returned by event enumeration.

If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA architecture, developers should use <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram">IWiaDevMgr::RegisterEventCallbackProgram</a> instead of this method.

<div class="alert"><b>Note</b>  In a multi-threaded application, there is no guarantee that the event notification callback will come in on the same thread that registered the callback.</div>
<div> </div>