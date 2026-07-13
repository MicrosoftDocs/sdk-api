---
UID: NS:swdevicedef._SW_DEVICE_CREATE_INFO
title: SW_DEVICE_CREATE_INFO (swdevicedef.h)
description: Describes info that PnP uses to create the software device.
helpviewer_keywords: ["*PSW_DEVICE_CREATE_INFO","PSW_DEVICE_CREATE_INFO","PSW_DEVICE_CREATE_INFO structure pointer","SWDeviceCapabilitiesDriverRequired","SWDeviceCapabilitiesNoDisplayInUI","SWDeviceCapabilitiesNone","SWDeviceCapabilitiesRemovable","SWDeviceCapabilitiesSilentInstall","SW_DEVICE_CREATE_INFO","SW_DEVICE_CREATE_INFO structure","swdevice.sw_device_create_info","swdevicedef/PSW_DEVICE_CREATE_INFO","swdevicedef/SW_DEVICE_CREATE_INFO"]
old-location: swdevice\sw_device_create_info.htm
tech.root: swdevice
ms.assetid: 9519FD17-AB43-4C9E-BE77-9DFAC3263447
ms.date: 07/23/2024
ms.keywords: '*PSW_DEVICE_CREATE_INFO, PSW_DEVICE_CREATE_INFO, PSW_DEVICE_CREATE_INFO structure pointer, SWDeviceCapabilitiesDriverRequired, SWDeviceCapabilitiesNoDisplayInUI, SWDeviceCapabilitiesNone, SWDeviceCapabilitiesRemovable, SWDeviceCapabilitiesSilentInstall, SW_DEVICE_CREATE_INFO, SW_DEVICE_CREATE_INFO structure, swdevice.sw_device_create_info, swdevicedef/PSW_DEVICE_CREATE_INFO, swdevicedef/SW_DEVICE_CREATE_INFO'
req.header: swdevicedef.h
req.include-header: Swdevice.h
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
req.typenames: SW_DEVICE_CREATE_INFO, *PSW_DEVICE_CREATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SW_DEVICE_CREATE_INFO
 - swdevicedef/_SW_DEVICE_CREATE_INFO
 - PSW_DEVICE_CREATE_INFO
 - swdevicedef/PSW_DEVICE_CREATE_INFO
 - SW_DEVICE_CREATE_INFO
 - swdevicedef/SW_DEVICE_CREATE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Swdevicedef.h
api_name:
 - SW_DEVICE_CREATE_INFO
---

# SW_DEVICE_CREATE_INFO structure


## -description

Describes info that PnP uses to create the software device.

## -struct-fields

### -field cbSize

The size in bytes of this structure. Use it as a version field.  Initialize it to sizeof(SW_DEVICE_CREATE_INFO).

### -field pszInstanceId

A string that represents the [instance ID](/windows-hardware/drivers/install/instance-ids) portion of the [device instance ID](/windows-hardware/drivers/install/device-instance-ids). This value is used for <a href="/windows-hardware/drivers/kernel/irp-mn-query-id">IRP_MN_QUERY_ID</a> <b>BusQueryInstanceID</b>.  Because all software devices are considered "UniqueId" devices, this string must be a unique name for all devices on this software device enumerator.

### -field pszzHardwareIds

A list of strings for the [hardware IDs](/windows-hardware/drivers/install/hardware-ids) for the software device. This value is used for <a href="/windows-hardware/drivers/kernel/irp-mn-query-id">IRP_MN_QUERY_ID</a> <b>BusQueryHardwareIDs</b>.  If a client expects a driver package to be installed on the device, the client should specify hardware IDs.

### -field pszzCompatibleIds

A list of strings for the [compatible IDs](/windows-hardware/drivers/install/compatible-ids) for the software device. This value is used for <a href="/windows-hardware/drivers/kernel/irp-mn-query-id">IRP_MN_QUERY_ID</a> <b>BusQueryCompatibleIDs</b>.  If a client expects a class driver package to be installed on the device, the client specifies compatible IDs that match the class driver package.  If a driver package isn't needed, we recommend to specify a compatible ID to classify the type of software device.  In addition to the compatible IDs specified in this member, `SWD\Generic` and possibly `SWD\GenericRaw` will always be added as the least specific compatible IDs.

### -field pContainerId

A value that is used to control the base container ID for the software device.  This value will be used for <a href="/windows-hardware/drivers/kernel/irp-mn-query-id">IRP_MN_QUERY_ID</a> <b>BusQueryContainerIDs</b>.  For typical situations, we recommend to set this member to <b>NULL</b> and use the <b>SWDeviceCapabilitiesRemovable</b> flag to control whether the device inherits the parent's container ID or if PnP assigns a new random container ID. See [Overview of the removable device capability](/windows-hardware/drivers/install/overview-of-the-removable-device-capability) for more information on how that affects the assignment of the container ID for the device. If the client needs to explicitly control the container ID, specify a <b>GUID</b> in the variable that this member points to. In general, you should not specify NULL_GUID for the container ID. See [Overview of container IDs](/windows-hardware/drivers/install/overview-of-container-ids) for more information on container IDs and the special meaning of NULL_GUID.

### -field CapabilityFlags

A combination of <b>SW_DEVICE_CAPABILITIES</b> values that are combined by using a bitwise OR operation. The resulting value specifies capabilities of the software device. The capabilities that you can specify when you create a software device are a subset of the capabilities that a bus driver can specify by using the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_device_capabilities"><b>DEVICE_CAPABILTIES</b></a> structure.  Only capabilities that make sense to allow changing for a software only device are supported.  The rest receive appropriate default values. Here are possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SWDeviceCapabilitiesNone"></a><a id="swdevicecapabilitiesnone"></a><a id="SWDEVICECAPABILITIESNONE"></a><dl>
<dt><b>SWDeviceCapabilitiesNone</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
No capabilities have been specified.

</td>
</tr>
<tr>
<td width="40%"><a id="SWDeviceCapabilitiesRemovable"></a><a id="swdevicecapabilitiesremovable"></a><a id="SWDEVICECAPABILITIESREMOVABLE"></a><dl>
<dt><b>SWDeviceCapabilitiesRemovable</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This bit specifies that the device is removable from its parent.  Setting this flag is equivalent to a bus driver setting the <b>Removable</b> member of the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_device_capabilities"><b>DEVICE_CAPABILTIES</b></a> structure for a PDO.

</td>
</tr>
<tr>
<td width="40%"><a id="SWDeviceCapabilitiesSilentInstall"></a><a id="swdevicecapabilitiessilentinstall"></a><a id="SWDEVICECAPABILITIESSILENTINSTALL"></a><dl>
<dt><b>SWDeviceCapabilitiesSilentInstall</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
This bit suppresses UI that would normally be shown during installation.  Setting this flag is equivalent to a bus driver setting the <b>SilentInstall</b> member of the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_device_capabilities"><b>DEVICE_CAPABILTIES</b></a> structure for a PDO.

</td>
</tr>
<tr>
<td width="40%"><a id="SWDeviceCapabilitiesNoDisplayInUI"></a><a id="swdevicecapabilitiesnodisplayinui"></a><a id="SWDEVICECAPABILITIESNODISPLAYINUI"></a><dl>
<dt><b>SWDeviceCapabilitiesNoDisplayInUI</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
This bit prevents the device from being displayed in some UI.  Setting this flag is equivalent to a bus driver setting the <b>NoDisplayInUI</b> member of the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_device_capabilities"><b>DEVICE_CAPABILTIES</b></a> structure for a PDO.

</td>
</tr>
<tr>
<td width="40%"><a id="SWDeviceCapabilitiesDriverRequired"></a><a id="swdevicecapabilitiesdriverrequired"></a><a id="SWDEVICECAPABILITIESDRIVERREQUIRED"></a><dl>
<dt><b>SWDeviceCapabilitiesDriverRequired</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Specify this bit when the client wants a driver to be loaded on the device and when this driver is required for correct function of the client’s feature.

When this bit is specified, at least one of <b>pszzHardwareIds</b> or <b>pszzCompatibleIds</b> must be filled in.

  If this bit is specified and if a driver can't be found, the device shows a yellow bang in <b>Device Manager</b> to indicate that the device has a problem, and Troubleshooters flag this as a device with a problem.  Setting this bit is equivalent to a bus driver not setting the <b>RawDeviceOK</b> member of the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_device_capabilities"><b>DEVICE_CAPABILTIES</b></a> structure for a PDO.

When this bit is specified, the driver owns creating interfaces for the device, and you can't call <a href="/windows/desktop/api/swdevice/nf-swdevice-swdeviceinterfaceregister">SwDeviceInterfaceRegister</a> for the device.

</td>
</tr>
</table>

### -field pszDeviceDescription

A string that contains the text that is displayed for the device name in the UI. This value is used for <a href="/windows-hardware/drivers/kernel/irp-mn-query-device-text">IRP_MN_QUERY_DEVICE_TEXT</a> <b>DeviceTextDescription</b>.  

<div class="alert"><b>Note</b>  <p class="note">When an INF is matched against the device, the name from the INF overrides this name unless steps are taken to preserve this name.

<p class="note">We recommend that this string be a reference to a localizable resource. For the syntax of referencing resources, see <a href="/windows-hardware/drivers/install/devprop-type-string-indirect">DEVPROP_TYPE_STRING_INDIRECT</a>. 

</div>
<div> </div>

### -field pszDeviceLocation

A string that contains the text that is displayed for the device location in the UI.  This value is used for <a href="/windows-hardware/drivers/kernel/irp-mn-query-device-text">IRP_MN_QUERY_DEVICE_TEXT</a> <b>DeviceTextLocationInformation</b>.  

<div class="alert"><b>Note</b>  Specifying a location is uncommon.</div>
<div> </div>

### -field pSecurityDescriptor

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the security information associated with the software device. If this member is <b>NULL</b>, the <a href="/windows-hardware/drivers/kernel/windows-kernel-mode-i-o-manager">I/O Manager</a> assigns the default security descriptor to the device.  If a custom security descriptor is needed, specify a self-relative security descriptor.

## -remarks

You can only specify this info at creation time, and you can't later call the Software Device API to modify this info, by setting properties, for example.

## -see-also

<a href="/windows/desktop/api/swdevice/nf-swdevice-swdevicecreate">SwDeviceCreate</a>