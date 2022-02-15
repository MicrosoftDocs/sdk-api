---
UID: NI:usbuser.IOCTL_USB_USER_REQUEST
title: IOCTL_USB_USER_REQUEST (usbuser.h)
description: The IOCTL_USB_USER_REQUEST I/O control request is available to both user-mode applications and kernel-mode drivers.
helpviewer_keywords: ["IOCTL_USB_USER_REQUEST","IOCTL_USB_USER_REQUEST control","IOCTL_USB_USER_REQUEST control code [Buses]","buses.ioctl_usb_user_request","usbirp_7409a5c0-756e-45ea-b2f5-0b73d91c9225.xml","usbuser/IOCTL_USB_USER_REQUEST"]
old-location: buses\ioctl_usb_user_request.htm
tech.root: buses
ms.assetid: 6aba5cf4-a9fa-4d10-a212-acc79e00fa9b
ms.date: 12/05/2018
ms.keywords: IOCTL_USB_USER_REQUEST, IOCTL_USB_USER_REQUEST control, IOCTL_USB_USER_REQUEST control code [Buses], buses.ioctl_usb_user_request, usbirp_7409a5c0-756e-45ea-b2f5-0b73d91c9225.xml, usbuser/IOCTL_USB_USER_REQUEST
req.header: usbuser.h
req.include-header: Usbuser.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCTL_USB_USER_REQUEST
 - usbuser/IOCTL_USB_USER_REQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usbuser.h
api_name:
 - IOCTL_USB_USER_REQUEST
---

# IOCTL_USB_USER_REQUEST IOCTL


## -description

The <b>IOCTL_USB_USER_REQUEST</b> I/O control request is available to both user-mode applications and kernel-mode drivers. 

<b>IOCTL_USB_USER_REQUEST</b> is a user-mode I/O control request. This request targets the USB host controller (GUID_DEVINTERFACE_USB_HOST_CONTROLLER).

Callers can specify any of the following request codes:


<dl>
<dt><a id="USBUSER_CLEAR_ROOTPORT_FEATURE"></a><a id="usbuser_clear_rootport_feature"></a>USBUSER_CLEAR_ROOTPORT_FEATURE</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_GET_CONTROLLER_DRIVER_KEY"></a><a id="usbuser_get_controller_driver_key"></a>USBUSER_GET_CONTROLLER_DRIVER_KEY</dt>
<dd>
Reports the host controller driver key in a <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_unicode_name">USB_UNICODE_NAME</a>-typed Unicode string. This request is always enabled.

</dd>
<dt><a id="USBUSER_GET_CONTROLLER_INFO_0"></a><a id="usbuser_get_controller_info_0"></a>USBUSER_GET_CONTROLLER_INFO_0</dt>
<dd>
Retrieves a <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_controller_info_0">USB_CONTROLLER_INFO_0</a> structure that describes the host controller. This request is always enabled.

</dd>
<dt><a id="USBUSER_GET_ROOTPORT_STATUS"></a><a id="usbuser_get_rootport_status"></a>USBUSER_GET_ROOTPORT_STATUS</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_GET_ROOTHUB_SYMBOLIC_NAME"></a><a id="usbuser_get_roothub_symbolic_name"></a>USBUSER_GET_ROOTHUB_SYMBOLIC_NAME</dt>
<dd>
Reports the root hub symbolic name in a <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_unicode_name">USB_UNICODE_NAME</a>-typed Unicode string. This request is always enabled.

</dd>
<dt><a id="USBUSER_INVALID_REQUEST"></a><a id="usbuser_invalid_request"></a>USBUSER_INVALID_REQUEST</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_OP_CLOSE_RAW_DEVICE"></a><a id="usbuser_op_close_raw_device"></a>USBUSER_OP_CLOSE_RAW_DEVICE</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_OP_OPEN_RAW_DEVICE"></a><a id="usbuser_op_open_raw_device"></a>USBUSER_OP_OPEN_RAW_DEVICE</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_OP_MASK_DEVONLY_API"></a><a id="usbuser_op_mask_devonly_api"></a>USBUSER_OP_MASK_DEVONLY_API</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_OP_MASK_HCTEST_API"></a><a id="usbuser_op_mask_hctest_api"></a>USBUSER_OP_MASK_HCTEST_API</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_OP_RAW_RESET_PORT"></a><a id="usbuser_op_raw_reset_port"></a>USBUSER_OP_RAW_RESET_PORT</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_OP_SEND_ONE_PACKET"></a><a id="usbuser_op_send_one_packet"></a>USBUSER_OP_SEND_ONE_PACKET</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_OP_SEND_RAW_COMMAND"></a><a id="usbuser_op_send_raw_command"></a>USBUSER_OP_SEND_RAW_COMMAND</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_SET_ROOTPORT_FEATURE"></a><a id="usbuser_set_rootport_feature"></a>USBUSER_SET_ROOTPORT_FEATURE</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_PASS_THRU"></a><a id="usbuser_pass_thru"></a>USBUSER_PASS_THRU</dt>
<dd>
Sends a vendor specific command that is defined by the <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_pass_thru_parameters">USB_PASS_THRU_PARAMETERS</a> structure to the host controller miniport driver. This request is always enabled.

</dd>
<dt><a id="USBUSER_GET_BANDWIDTH_INFORMATION"></a><a id="usbuser_get_bandwidth_information"></a>USBUSER_GET_BANDWIDTH_INFORMATION</dt>
<dd>
Retrieves a <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_bandwidth_info">USB_BANDWIDTH_INFO</a> structure that contains information about the allocated bandwidth. This request is always enabled.

</dd>
<dt><a id="USBUSER_GET_POWER_STATE_MAP"></a><a id="usbuser_get_power_state_map"></a>USBUSER_GET_POWER_STATE_MAP</dt>
<dd>
Retrieves a <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_power_info">USB_POWER_INFO</a> structure that contains information about the power state of the host controller and root hubs. This request is always enabled.

</dd>
<dt><a id="USBUSER_GET_BUS_STATISTICS_0"></a><a id="usbuser_get_bus_statistics_0"></a>USBUSER_GET_BUS_STATISTICS_0</dt>
<dd>
Retrieves a <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_bus_statistics_0">USB_BUS_STATISTICS_0</a> structure that contains bus statistics. This request is always enabled.

</dd>
<dt><a id="USBUSER_GET_BUS_STATISTICS_0_AND_RESET"></a><a id="usbuser_get_bus_statistics_0_and_reset"></a>USBUSER_GET_BUS_STATISTICS_0_AND_RESET</dt>
<dd>
Do not use this request.

</dd>
<dt><a id="USBUSER_GET_USB_DRIVER_INFORMATION"></a><a id="usbuser_get_usb_driver_information"></a>USBUSER_GET_USB_DRIVER_INFORMATION</dt>
<dd>
Retrieves a <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_driver_version_parameters">USB_DRIVER_VERSION_PARAMETERS</a> structure that indicates the version of the driver, USB stack, and associated interfaces. This request is always enabled.

</dd>
<dt><a id="USBUSER_GET_USB2_HW_VERSION"></a><a id="usbuser_get_usb2_hw_version"></a>USBUSER_GET_USB2_HW_VERSION</dt>
<dd>
Do not use this request.

</dd>
</dl>

## -ioctlparameters

### -input-buffer

The buffer at <b>Irp-&gt;AssociatedIrp.SystemBuffer</b> contains a user request header structure (<a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a>) that defines the request. Following the header structure is a structure that holds the parameters of the request. For more information about the parameter structures that correspond to each request, see the description of each request.

### -input-buffer-length

The size of a <a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a> structure.

### -output-buffer

A parameter structure immediately follows the <a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a> structure at <b>Irp-&gt;AssociatedIrp.SystemBuffer</b>. For some user requests, the parameter structure will contain output data when the request completes.

### -output-buffer-length

The length of the parameter structure.

### -in-out-buffer


### -inout-buffer-length


### -status-block

The USB stack sets <b>Irp-&gt;IoStatus.Status</b> to STATUS_SUCCESS if the request is successful. Otherwise, the USB stack sets <b>Status</b> to the appropriate error condition, such as STATUS_INVALID_PARAMETER or STATUS_INSUFFICIENT_RESOURCES.

## -see-also

<a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_bandwidth_info">USB_BANDWIDTH_INFO</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_controller_info_0">USB_CONTROLLER_INFO_0</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_driver_version_parameters">USB_DRIVER_VERSION_PARAMETERS</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_pass_thru_parameters">USB_PASS_THRU_PARAMETERS</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_power_info">USB_POWER_INFO</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_unicode_name">USB_UNICODE_NAME</a>