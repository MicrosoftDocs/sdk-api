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

# _CM_NOTIFY_ACTION enumeration


## -description


This enumeration identifies Plug and Play device event types.


## -enum-fields




### -field CM_NOTIFY_ACTION_DEVICEINTERFACEARRIVAL

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINTERFACE</b>.  This action indicates that a device interface that meets your filter criteria has been enabled.


### -field CM_NOTIFY_ACTION_DEVICEINTERFACEREMOVAL

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINTERFACE</b>.

  This action indicates that a device interface that meets your filter criteria has been disabled.


### -field CM_NOTIFY_ACTION_DEVICEQUERYREMOVE

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

  This action indicates that the device is being query removed.  In order to allow the query remove to succeed, call <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> to close any handles you have open to the device. If you do not do this, your open handle prevents the query remove of this device from succeeding.  See <a href="devinst.registering_for_notification_of_device_interface_arrival_and_device_removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information.

To veto the query remove, return ERROR_CANCELLED.  However, it is recommended that you do not veto the query remove and allow it to happen by closing any handles you have open to the device.


### -field CM_NOTIFY_ACTION_DEVICEQUERYREMOVEFAILED

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

 This action indicates that the query remove of a device was failed.  If you closed the handle to this device during a previous notification of <b>CM_NOTIFY_ACTION_DEVICEQUERYREMOVE</b>, open a new handle to the device to continue sending I/O requests to it.  See <a href="devinst.registering_for_notification_of_device_interface_arrival_and_device_removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information.


### -field CM_NOTIFY_ACTION_DEVICEREMOVEPENDING

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

The device will be removed.  If you still have an open handle to the device, call <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> to close the device handle. See <a href="devinst.registering_for_notification_of_device_interface_arrival_and_device_removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information. The system may send a <b>CM_NOTIFY_ACTION_DEVICEREMOVEPENDING</b> notification without sending a corresponding <b>CM_NOTIFY_ACTION_DEVICEQUERYREMOVE</b> message.  In such cases, the applications and drivers must recover from the loss of the device as best they can.


### -field CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

The device has been removed.  If you still have an open handle to the device, call <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> to close the device handle. See <a href="devinst.registering_for_notification_of_device_interface_arrival_and_device_removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information.  The system may send a <b>CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE</b> notification without sending corresponding <b>CM_NOTIFY_ACTION_DEVICEQUERYREMOVE</b> or <b>CM_NOTIFY_ACTION_DEVICEREMOVEPENDING</b> messages.  In such cases, the applications and drivers must recover from the loss of the device as best they can.


### -field CM_NOTIFY_ACTION_DEVICECUSTOMEVENT

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>. This action is sent when a driver-defined custom event has occurred.


### -field CM_NOTIFY_ACTION_DEVICEINSTANCEENUMERATED

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE</b>. This action is sent when a new device instance that meets your filter criteria has been enumerated.


### -field CM_NOTIFY_ACTION_DEVICEINSTANCESTARTED

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE</b>. This action is sent when a device instance that meets your filter criteria becomes started. 


### -field CM_NOTIFY_ACTION_DEVICEINSTANCEREMOVED

For this value, set the <b>FilterType</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE</b>. This action is sent when a device instance that meets your filter criteria is no longer present.


### -field CM_NOTIFY_ACTION_MAX

Do not use.


## -remarks



When a driver calls the <a href="https://msdn.microsoft.com/library/windows/hardware/hh780224">CM_Register_Notification</a> function, the <i>pCallback</i> parameter contains a pointer to a routine to be called when a specified PnP event occurs.  The callback routine's <i>Action</i> parameter is a value from the <b>CM_NOTIFY_ACTION</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt299055">CM_NOTIFY_FILTER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh780224">CM_Register_Notification</a>
 

 

