---
UID: NF:winuser.RegisterPowerSettingNotification
title: RegisterPowerSettingNotification function
author: windows-sdk-content
description: Registers the application to receive power setting notifications for the specific power setting event.
old-location: base\registerpowersettingnotification.htm
tech.root: power
ms.assetid: e072222e-da66-4b36-a38f-f4b618eaa391
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DEVICE_NOTIFY_SERVICE_HANDLE, DEVICE_NOTIFY_WINDOW_HANDLE, RegisterPowerSettingNotification, RegisterPowerSettingNotification function, base.registerpowersettingnotification, winuser/RegisterPowerSettingNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-powermanagement-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-powermanagement-l1-1-0.dll
api_name:
 - RegisterPowerSettingNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterPowerSettingNotification function


## -description


Registers the application to receive power setting notifications for the specific power setting event.


## -parameters




### -param hRecipient [in]

Handle indicating where the power setting notifications are to be sent. For interactive applications, the 
     <i>Flags</i> parameter should be zero, and the <i>hRecipient</i> parameter 
     should be a window handle. For services, the <i>Flags</i> parameter should be one, and the 
     <i>hRecipient</i> parameter should be a <b>SERVICE_STATUS_HANDLE</b> 
     as returned from 
     <a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a>.


### -param PowerSettingGuid [in]

The <b>GUID</b> of the power setting for which notifications are to be sent. For more information see <a href="https://msdn.microsoft.com/840390ca-d32a-4cf3-9e75-66322c7cdee0">Registering for Power 
      Events</a>.


### -param Flags [in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_WINDOW_HANDLE"></a><a id="device_notify_window_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_WINDOW_HANDLE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Notifications are sent using <a href="https://msdn.microsoft.com/46452909-ac0e-4c06-8542-0b94d00e6556">WM_POWERBROADCAST</a> 
       messages with a <i>wParam</i> parameter of 
       <a href="https://msdn.microsoft.com/0bcadb85-47c5-48a9-b3f9-f0a1ca60b503">PBT_POWERSETTINGCHANGE</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_SERVICE_HANDLE"></a><a id="device_notify_service_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_SERVICE_HANDLE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Notifications are sent to the <a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a> callback 
       function with a <i>dwControl</i> parameter of 
       <b>SERVICE_CONTROL_POWEREVENT</b> and a <i>dwEventType</i> of 
       <a href="https://msdn.microsoft.com/0bcadb85-47c5-48a9-b3f9-f0a1ca60b503">PBT_POWERSETTINGCHANGE</a>.

</td>
</tr>
</table>
 


## -returns



Returns a notification handle for unregistering for power notifications. If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/840390ca-d32a-4cf3-9e75-66322c7cdee0">Registering for Power Events</a>



<a href="https://msdn.microsoft.com/de1509f5-cf4c-448e-bb3b-08da6be53bfa">UnregisterPowerSettingNotification</a>
 

 

