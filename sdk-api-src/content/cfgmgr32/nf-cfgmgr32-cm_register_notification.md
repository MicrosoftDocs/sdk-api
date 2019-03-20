---
UID: NF:cfgmgr32.CM_Register_Notification
title: CM_Register_Notification function (cfgmgr32.h)
author: windows-sdk-content
description: Use RegisterDeviceNotification instead of CM_Register_Notification if your code targets Windows 7 or earlier versions of Windows. Kernel mode callers should use IoRegisterPlugPlayNotification instead.
old-location: devinst\cm_register_notification.htm
tech.root: devinst
ms.assetid: 15847F9C-9F2A-453F-9EF8-0AF63CFF93C9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Register_Notification, CM_Register_Notification function [Device and Driver Installation], cfgmgr32/CM_Register_Notification, devinst.cm_register_notification
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 8 and later versions of Windows.
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
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Register_Notification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Register_Notification function


## -description


Use <a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a> instead of <b>CM_Register_Notification</b> if your code targets Windows 7 or earlier versions of Windows. Kernel mode callers should use <a href="https://msdn.microsoft.com/06fd10ab-3478-4b01-b678-24944f17fa9d">IoRegisterPlugPlayNotification</a> instead.

The <b>CM_Register_Notification</b> function registers an application callback routine to be called when a PnP event of the specified type occurs.


## -parameters




### -param pFilter [in]

Pointer to a <a href="https://msdn.microsoft.com/8B6CC440-7B41-4382-9917-6833031D5E1B">CM_NOTIFY_FILTER</a> structure.


### -param pContext [in, optional]

Pointer to a caller-allocated buffer containing the context to be passed to the callback routine in <i>pCallback</i>.


### -param pCallback [in]

Pointer to the routine to be called when the specified PnP event occurs. See the <b>Remarks</b> section for the callback function's prototype.

The callback routine’s <i>Action</i> parameter will be a value from the <a href="https://msdn.microsoft.com/587AF979-8BA2-45A3-90C2-7E0EBB2390EC">CM_NOTIFY_ACTION</a> enumeration.

Upon receiving a notification, how the callback examines the notification will depend on the <b>FilterType</b> member of the callback routine's <i>EventData</i> parameter:





#### CM_NOTIFY_FILTER_TYPE_DEVICEINTERFACE

The callback should examine <b>EventData-&gt;u.DeviceInterface</b>.



#### CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE

The callback should examine <b>EventData-&gt;u.DeviceHandle</b>.



#### CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE

The callback should examine <b>EventData-&gt;u.DeviceInstance</b>.


### -param pNotifyContext [out]

Pointer to receive the HCMNOTIFICATION handle that corresponds to the registration call.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Be sure to handle Plug and Play device events as quickly as possible.  If your event handler performs any operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.

The <b>CM_Register_Notification</b> function does not provide notification of existing device interfaces.   To retrieve existing interfaces, first call <b>CM_Register_Notification</b>, and then call <a href="https://msdn.microsoft.com/3f2dfc0f-1bde-40a8-b48c-25b75759e0d8">CM_Get_Device_Interface_List</a>.   If the interface is enabled after your driver calls <b>CM_Register_Notification</b>, but before your driver calls <b>CM_Get_Device_Interface_List</b>, the driver receives a notification for the interface arrival, and the interface also appears in the list of device interface instances returned by <b>CM_Get_Device_Interface_List</b>.

HCMNOTIFICATION handles returned by <b>CM_Register_Notification</b> must be closed by calling the <a href="https://msdn.microsoft.com/1634ECC5-96A2-4B1C-8DCA-64682C8C1444">CM_Unregister_Notification</a> function when they are no longer needed.

A callback routine uses the following function prototype:
		  


```
typedef __callback DWORD (CALLBACK *PCM_NOTIFY_CALLBACK)(
    _In_ HCMNOTIFICATION       hNotify,
    _In_opt_ PVOID             Context,
    _In_ CM_NOTIFY_ACTION      Action,
    _In_reads_bytes_(EventDataSize) PCM_NOTIFY_EVENT_DATA EventData,
    _In_ DWORD                 EventDataSize
    );
```


If responding to a <b>CM_NOTIFY_ACTION_DEVICEQUERYREMOVE</b> notification, the PCM_NOTIFY_CALLBACK callback should return either ERROR_SUCCESS or ERROR_CANCELLED, as appropriate.  Otherwise, the callback should return ERROR_SUCCESS. The callback should not return any other values. For a description of other actions, please refer to the <a href="https://msdn.microsoft.com/587AF979-8BA2-45A3-90C2-7E0EBB2390EC">CM_NOTIFY_ACTION</a> documentation.  Also see <a href="https://msdn.microsoft.com/61bd4ea3-9910-4feb-a330-3e0bcdac1ce2">CM_NOTIFY_EVENT_DATA</a> for information about the structure that this callback receives in the <i>EventData</i> parameter.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/library/Dn858592(v=VS.85).aspx">Registering for Notification of Device Interface Arrival and Device Removal</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/587AF979-8BA2-45A3-90C2-7E0EBB2390EC">CM_NOTIFY_ACTION</a>



<a href="https://msdn.microsoft.com/8B6CC440-7B41-4382-9917-6833031D5E1B">CM_NOTIFY_FILTER</a>



<a href="https://msdn.microsoft.com/1634ECC5-96A2-4B1C-8DCA-64682C8C1444">CM_Unregister_Notification</a>



<a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a>



<a href="https://msdn.microsoft.com/library/Dn858592(v=VS.85).aspx">Registering for Notification of Device Interface Arrival and Device Removal</a>



<a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-device-interfaces">Using Device Interfaces</a>
 

 

