---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

Specifies the event for which the application is registering. For a list of standard events, see <a href="https://msdn.microsoft.com/b94221b3-7cab-40d7-850a-fcc4ec8174b5">WIA Event Identifiers</a>.


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



WIA applications use this method to register to receive hardware device events of the type WIA_ACTION_EVENT. Once programs call <b>IWiaDevMgr::RegisterEventCallbackCLSID</b>, they are registered to receive WIA device events even if they are not running. 

When the event occurs, the WIA system determines which application is registered to receive the event. It uses the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function and the class ID specified in the <i>pClsID</i> parameter to create an instance of the application. It then calls the application's <a href="https://msdn.microsoft.com/0aab6a63-07af-4833-b021-309300ea7343">ImageEventCallback</a> method to transmit the event information.

An application can invoke the <a href="https://msdn.microsoft.com/fb35f225-3831-4442-b1e7-6314f59d158a">EnumRegisterEventInfo</a> method to enumerate event registration information.

An application can find whether an event is an action type or notification type (or both) event by examinging the <b>ulFlags</b> value of a <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structure returned by event enumeration.

If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA architecture, developers should use <a href="https://msdn.microsoft.com/177438ff-afeb-4499-9870-647c49209a6e">IWiaDevMgr::RegisterEventCallbackProgram</a> instead of this method.

<div class="alert"><b>Note</b>  In a multi-threaded application, there is no guarantee that the event notification callback will come in on the same thread that registered the callback.</div>
<div> </div>


