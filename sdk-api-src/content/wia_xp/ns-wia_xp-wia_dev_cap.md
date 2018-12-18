---
UID: NS:wia_xp._WIA_DEV_CAP
title: WIA_DEV_CAP
author: windows-sdk-content
description: Applications use the WIA_DEV_CAP structure to enumerate device capabilities. A device capability is defined by an event or command that the device supports. For more information, see IEnumWIA_DEV_CAPS.
old-location: wia\_wia_WIA_DEV_CAP.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_dev_cap.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWIA_DEV_CAP, *PWIA_EVENT_HANDLER, PWIA_DEV_CAP, PWIA_DEV_CAP structure pointer [WIA], PWIA_EVENT_HANDLER, PWIA_EVENT_HANDLER structure pointer [WIA], WIA_DEV_CAP, WIA_DEV_CAP structure [WIA], WIA_EVENT_HANDLER, WIA_EVENT_HANDLER structure [WIA], _wia_WIA_DEV_CAP, wia._wia_WIA_DEV_CAP, wia_xp/PWIA_DEV_CAP, wia_xp/PWIA_EVENT_HANDLER, wia_xp/WIA_DEV_CAP, wia_xp/WIA_EVENT_HANDLER"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wia_xp.h
api_name:
 - WIA_DEV_CAP
product: Windows
targetos: Windows
req.typenames: WIA_DEV_CAP, *PWIA_DEV_CAP, WIA_EVENT_HANDLER, *PWIA_EVENT_HANDLER
req.redist: 
---

# WIA_DEV_CAP structure


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

