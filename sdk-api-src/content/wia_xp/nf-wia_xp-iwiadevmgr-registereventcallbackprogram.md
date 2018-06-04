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

Specifies the event for which the application is registering. For a list of valid event GUIDs, see <a href="https://msdn.microsoft.com/b94221b3-7cab-40d7-850a-fcc4ec8174b5">WIA Event Identifiers</a>.


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use <b>IWiaDevMgr::RegisterEventCallbackProgram</b> to register for hardware device events of the type WIA_ACTION_EVENT. When an event occurs for which an application is registered, the application is launched and the event information is transmitted to the application.

Applications use the <a href="https://msdn.microsoft.com/fb35f225-3831-4442-b1e7-6314f59d158a">EnumRegisterEventInfo</a> method to retrieve a pointer to an enumerator object for event registration properties.

An application can find whether an event is an action type or notification type (or both) event by examinging the <b>ulFlags</b> value of a <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structure returned by event enumeration.

Programs should only use the <b>IWiaDevMgr::RegisterEventCallbackProgram</b> method for backward compatibility with applications not written for the WIA architecture. New applications should use the Component Object Model (COM) interfaces provided by the WIA architecture. Specifically, they should call <a href="https://msdn.microsoft.com/81a5bb61-5ec6-4c0b-8627-faccaf54d05a">IWiaDevMgr::RegisterEventCallbackInterface</a> or <a href="https://msdn.microsoft.com/71f1f7f9-583a-423c-bf96-2c2596808079">IWiaDevMgr::RegisterEventCallbackCLSID</a> to register for device events.

Typically, this method is called by an install program or a script. The install program or script registers the application to receive WIA device events. When the event occurs, the application will be started by the WIA run-time system.



