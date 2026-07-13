---
UID: NF:wia_xp.IWiaDevMgr.RegisterEventCallbackProgram
title: IWiaDevMgr::RegisterEventCallbackProgram (wia_xp.h)
description: The IWiaDevMgr::RegisterEventCallbackProgram method registers an application to receive device events. It is primarily provided for backward compatibility with applications that were not written for WIA.
helpviewer_keywords: ["IWiaDevMgr interface [WIA]","RegisterEventCallbackProgram method","IWiaDevMgr.RegisterEventCallbackProgram","IWiaDevMgr::RegisterEventCallbackProgram","RegisterEventCallbackProgram","RegisterEventCallbackProgram method [WIA]","RegisterEventCallbackProgram method [WIA]","IWiaDevMgr interface","_wia_IWiaDevMgr_RegisterEventCallbackProgram","wia._wia_IWiaDevMgr_RegisterEventCallbackProgram","wia_xp/IWiaDevMgr::RegisterEventCallbackProgram"]
old-location: wia\_wia_IWiaDevMgr_RegisterEventCallbackProgram.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\registereventcallbackprogram.htm
ms.date: 12/05/2018
ms.keywords: IWiaDevMgr interface [WIA],RegisterEventCallbackProgram method, IWiaDevMgr.RegisterEventCallbackProgram, IWiaDevMgr::RegisterEventCallbackProgram, RegisterEventCallbackProgram, RegisterEventCallbackProgram method [WIA], RegisterEventCallbackProgram method [WIA],IWiaDevMgr interface, _wia_IWiaDevMgr_RegisterEventCallbackProgram, wia._wia_IWiaDevMgr_RegisterEventCallbackProgram, wia_xp/IWiaDevMgr::RegisterEventCallbackProgram
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
 - IWiaDevMgr::RegisterEventCallbackProgram
 - wia_xp/IWiaDevMgr::RegisterEventCallbackProgram
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
 - IWiaDevMgr.RegisterEventCallbackProgram
archived: true
---

# IWiaDevMgr::RegisterEventCallbackProgram


## -description

The <b>IWiaDevMgr::RegisterEventCallbackProgram</b> method registers an application to receive device events. It is primarily provided for backward compatibility with applications that were not written for WIA.

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

Specifies the event for which the application is registering. For a list of valid event GUIDs, see <a href="/windows/desktop/wia/-wia-wia-event-identifiers">WIA Event Identifiers</a>.

### -param bstrCommandline [in]

Type: <b>BSTR</b>

Specifies a string that contains the full path name and the appropriate command-line arguments needed to invoke the application. Two pairs of quotation marks should be used, for example, "\"C:\Program Files\MyExe.exe\" /arg1".

### -param bstrName [in]

Type: <b>BSTR</b>

Specifies the name of the application. This name is displayed to the user when multiple applications register for the same event.

### -param bstrDescription [in]

Type: <b>BSTR</b>

Specifies the description of the application. This description is displayed to the user when multiple applications register for the same event.

### -param bstrIcon [in]

Type: <b>BSTR</b>

Specifies the icon that represents the application. The icon is displayed to the user when multiple applications register for the same event. The string contains the name of the application and the 0-based index of the icon (there may be more than one icon that represent application) separated by a comma. For example, "MyApp, 0".

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use <b>IWiaDevMgr::RegisterEventCallbackProgram</b> to register for hardware device events of the type WIA_ACTION_EVENT. When an event occurs for which an application is registered, the application is launched and the event information is transmitted to the application.

Applications use the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo">EnumRegisterEventInfo</a> method to retrieve a pointer to an enumerator object for event registration properties.

An application can find whether an event is an action type or notification type (or both) event by examining the <b>ulFlags</b> value of a <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_dev_cap">WIA_DEV_CAP</a> structure returned by event enumeration.

Programs should only use the <b>IWiaDevMgr::RegisterEventCallbackProgram</b> method for backward compatibility with applications not written for the WIA architecture. New applications should use the Component Object Model (COM) interfaces provided by the WIA architecture. Specifically, they should call <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface">IWiaDevMgr::RegisterEventCallbackInterface</a> or <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid">IWiaDevMgr::RegisterEventCallbackCLSID</a> to register for device events.

Typically, this method is called by an install program or a script. The install program or script registers the application to receive WIA device events. When the event occurs, the application will be started by the WIA run-time system.