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

# _WIA_DEV_CAP structure


## -description


Applications use the <b>WIA_DEV_CAP</b> structure to enumerate device capabilities. A device capability is defined by an event or command that the device supports. For more information, see <a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a>.


## -struct-fields




### -field guid

Type: <b>GUID</b>

Specifies a GUID that identifies the device capability. This member can be set to any of the values specified in <a href="https://msdn.microsoft.com/f86a0944-2f2a-467e-a9e8-4cdecfc50175">WIA Device Commands</a> or <a href="https://msdn.microsoft.com/b94221b3-7cab-40d7-850a-fcc4ec8174b5">WIA Event Identifiers</a>.


### -field ulFlags

Type: <b>ULONG</b>

Used when enumerating event handlers. The possible values are listed in this table.
                

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>WIA_IS_DEFAULT_HANDLER</td>
<td>The currently registered handler should be used. This is the only valid value when enumerating event handlers. It is not a valid value when enumerating event capabilities of a device.</td>
</tr>
<tr>
<td>WIA_ACTION_EVENT</td>
<td>The event is of the action type, so programs that use persistent registration APIs, <a href="https://msdn.microsoft.com/177438ff-afeb-4499-9870-647c49209a6e">IWiaDevMgr::RegisterEventCallbackProgram</a> and <a href="https://msdn.microsoft.com/71f1f7f9-583a-423c-bf96-2c2596808079">IWiaDevMgr::RegisterEventCallbackCLSID</a>, can receive it. </td>
</tr>
<tr>
<td>WIA_NOTIFICATION_EVENT</td>
<td>The event is of the notification type, so programs that use the runtime registration function, <a href="https://msdn.microsoft.com/81a5bb61-5ec6-4c0b-8627-faccaf54d05a">IWiaDevMgr::RegisterEventCallbackInterface</a>, can receive it. </td>
</tr>
</table>
 


### -field bstrName

Type: <b>BSTR</b>

Specifies a string that contains a short version of the capability name.


### -field bstrDescription

Type: <b>BSTR</b>

Specifies a string that contains a description of the capability that is displayed to the user.


### -field bstrIcon

Type: <b>BSTR</b>

Specifies a string that represents the location and resource ID of the icon that represents this capability or handler. The string must be of the following form: <i>drive</i><b>:\</b><i>path</i><b>\</b><i>module</i><b>,</b><i>n</i>, where <i>n</i> is the icon's negated resource ID (that is, if the resource ID of the icon is 100, then <i>n</i> is -100).


### -field bstrCommandline

Type: <b>BSTR</b>

Specifies a string that represents command line arguments.

