---
UID: NE:cfgmgr32._CM_NOTIFY_ACTION
title: CM_NOTIFY_ACTION (cfgmgr32.h)
description: This enumeration identifies Plug and Play device event types.
helpviewer_keywords: ["*PCM_NOTIFY_ACTION","CM_NOTIFY_ACTION","CM_NOTIFY_ACTION enumeration [Device and Driver Installation]","CM_NOTIFY_ACTION_DEVICECUSTOMEVENT","CM_NOTIFY_ACTION_DEVICEINSTANCEENUMERATED","CM_NOTIFY_ACTION_DEVICEINSTANCEREMOVED","CM_NOTIFY_ACTION_DEVICEINSTANCESTARTED","CM_NOTIFY_ACTION_DEVICEINTERFACEARRIVAL","CM_NOTIFY_ACTION_DEVICEINTERFACEREMOVAL","CM_NOTIFY_ACTION_DEVICEQUERYREMOVE","CM_NOTIFY_ACTION_DEVICEQUERYREMOVEFAILED","CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE","CM_NOTIFY_ACTION_DEVICEREMOVEPENDING","CM_NOTIFY_ACTION_MAX","cfgmgr32/CM_NOTIFY_ACTION","cfgmgr32/CM_NOTIFY_ACTION_DEVICECUSTOMEVENT","cfgmgr32/CM_NOTIFY_ACTION_DEVICEINSTANCEENUMERATED","cfgmgr32/CM_NOTIFY_ACTION_DEVICEINSTANCEREMOVED","cfgmgr32/CM_NOTIFY_ACTION_DEVICEINSTANCESTARTED","cfgmgr32/CM_NOTIFY_ACTION_DEVICEINTERFACEARRIVAL","cfgmgr32/CM_NOTIFY_ACTION_DEVICEINTERFACEREMOVAL","cfgmgr32/CM_NOTIFY_ACTION_DEVICEQUERYREMOVE","cfgmgr32/CM_NOTIFY_ACTION_DEVICEQUERYREMOVEFAILED","cfgmgr32/CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE","cfgmgr32/CM_NOTIFY_ACTION_DEVICEREMOVEPENDING","cfgmgr32/CM_NOTIFY_ACTION_MAX","devinst.cm_notify_action"]
old-location: devinst\cm_notify_action.htm
tech.root: devinst
ms.assetid: 587AF979-8BA2-45A3-90C2-7E0EBB2390EC
ms.date: 12/05/2018
ms.keywords: '*PCM_NOTIFY_ACTION, CM_NOTIFY_ACTION, CM_NOTIFY_ACTION enumeration [Device and Driver Installation], CM_NOTIFY_ACTION_DEVICECUSTOMEVENT, CM_NOTIFY_ACTION_DEVICEINSTANCEENUMERATED, CM_NOTIFY_ACTION_DEVICEINSTANCEREMOVED, CM_NOTIFY_ACTION_DEVICEINSTANCESTARTED, CM_NOTIFY_ACTION_DEVICEINTERFACEARRIVAL, CM_NOTIFY_ACTION_DEVICEINTERFACEREMOVAL, CM_NOTIFY_ACTION_DEVICEQUERYREMOVE, CM_NOTIFY_ACTION_DEVICEQUERYREMOVEFAILED, CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE, CM_NOTIFY_ACTION_DEVICEREMOVEPENDING, CM_NOTIFY_ACTION_MAX, cfgmgr32/CM_NOTIFY_ACTION, cfgmgr32/CM_NOTIFY_ACTION_DEVICECUSTOMEVENT, cfgmgr32/CM_NOTIFY_ACTION_DEVICEINSTANCEENUMERATED, cfgmgr32/CM_NOTIFY_ACTION_DEVICEINSTANCEREMOVED, cfgmgr32/CM_NOTIFY_ACTION_DEVICEINSTANCESTARTED, cfgmgr32/CM_NOTIFY_ACTION_DEVICEINTERFACEARRIVAL, cfgmgr32/CM_NOTIFY_ACTION_DEVICEINTERFACEREMOVAL, cfgmgr32/CM_NOTIFY_ACTION_DEVICEQUERYREMOVE, cfgmgr32/CM_NOTIFY_ACTION_DEVICEQUERYREMOVEFAILED, cfgmgr32/CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE, cfgmgr32/CM_NOTIFY_ACTION_DEVICEREMOVEPENDING, cfgmgr32/CM_NOTIFY_ACTION_MAX, devinst.cm_notify_action'
req.header: cfgmgr32.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CM_NOTIFY_ACTION
 - cfgmgr32/_CM_NOTIFY_ACTION
 - PCM_NOTIFY_ACTION
 - cfgmgr32/PCM_NOTIFY_ACTION
 - CM_NOTIFY_ACTION
 - cfgmgr32/CM_NOTIFY_ACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cfgmgr32.h
api_name:
 - CM_NOTIFY_ACTION
---

# CM_NOTIFY_ACTION enumeration


## -description

This enumeration identifies Plug and Play device event types.

## -enum-fields

### -field CM_NOTIFY_ACTION_DEVICEINTERFACEARRIVAL:0

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINTERFACE</b>.  This action indicates that a device interface that meets your filter criteria has been enabled.

### -field CM_NOTIFY_ACTION_DEVICEINTERFACEREMOVAL

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINTERFACE</b>.

  This action indicates that a device interface that meets your filter criteria has been disabled.

### -field CM_NOTIFY_ACTION_DEVICEQUERYREMOVE

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

  This action indicates that the device is being query removed.  In order to allow the query remove to succeed, call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> to close any handles you have open to the device. If you do not do this, your open handle prevents the query remove of this device from succeeding.  See <a href="/windows-hardware/drivers/install/registering-for-notification-of-device-interface-arrival-and-device-removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information.

To veto the query remove, return ERROR_CANCELLED.  However, it is recommended that you do not veto the query remove and allow it to happen by closing any handles you have open to the device.

### -field CM_NOTIFY_ACTION_DEVICEQUERYREMOVEFAILED

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

 This action indicates that the query remove of a device was failed.  If you closed the handle to this device during a previous notification of <b>CM_NOTIFY_ACTION_DEVICEQUERYREMOVE</b>, open a new handle to the device to continue sending I/O requests to it.  See <a href="/windows-hardware/drivers/install/registering-for-notification-of-device-interface-arrival-and-device-removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information.

### -field CM_NOTIFY_ACTION_DEVICEREMOVEPENDING

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

The device will be removed.  If you still have an open handle to the device, call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> to close the device handle. See <a href="/windows-hardware/drivers/install/registering-for-notification-of-device-interface-arrival-and-device-removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information. The system may send a <b>CM_NOTIFY_ACTION_DEVICEREMOVEPENDING</b> notification without sending a corresponding <b>CM_NOTIFY_ACTION_DEVICEQUERYREMOVE</b> message.  In such cases, the applications and drivers must recover from the loss of the device as best they can.

### -field CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>.

The device has been removed.  If you still have an open handle to the device, call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> to close the device handle. See <a href="/windows-hardware/drivers/install/registering-for-notification-of-device-interface-arrival-and-device-removal">Registering for Notification of Device Interface Arrival and Device Removal</a> for more information.  The system may send a <b>CM_NOTIFY_ACTION_DEVICEREMOVECOMPLETE</b> notification without sending corresponding <b>CM_NOTIFY_ACTION_DEVICEQUERYREMOVE</b> or <b>CM_NOTIFY_ACTION_DEVICEREMOVEPENDING</b> messages.  In such cases, the applications and drivers must recover from the loss of the device as best they can.

### -field CM_NOTIFY_ACTION_DEVICECUSTOMEVENT

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE</b>. This action is sent when a driver-defined custom event has occurred.

### -field CM_NOTIFY_ACTION_DEVICEINSTANCEENUMERATED

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE</b>. This action is sent when a new device instance that meets your filter criteria has been enumerated.

### -field CM_NOTIFY_ACTION_DEVICEINSTANCESTARTED

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE</b>. This action is sent when a device instance that meets your filter criteria becomes started.

### -field CM_NOTIFY_ACTION_DEVICEINSTANCEREMOVED

For this value, set the <b>FilterType</b> member of the <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a> structure
 to <b>CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE</b>. This action is sent when a device instance that meets your filter criteria is no longer present.

### -field CM_NOTIFY_ACTION_MAX

Do not use.

## -remarks

When a driver calls the <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_register_notification">CM_Register_Notification</a> function, the <i>pCallback</i> parameter contains a pointer to a routine to be called when a specified PnP event occurs.  The callback routine's <i>Action</i> parameter is a value from the <b>CM_NOTIFY_ACTION</b> enumeration.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cm_notify_filter">CM_NOTIFY_FILTER</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_register_notification">CM_Register_Notification</a>
