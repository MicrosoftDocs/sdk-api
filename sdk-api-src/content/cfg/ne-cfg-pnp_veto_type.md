---
UID: NE:cfg._PNP_VETO_TYPE
title: PNP_VETO_TYPE (cfg.h)
description: If the PnP manager rejects a request to perform an operation, the PNP_VETO_TYPE enumeration is used to identify the reason for the rejection.
helpviewer_keywords: ["*PPNP_VETO_TYPE","PNP_VETO_TYPE","PNP_VETO_TYPE enumeration [Device and Driver Installation]","PNP_VetoDevice","PNP_VetoDriver","PNP_VetoIllegalDeviceRequest","PNP_VetoInsufficientPower","PNP_VetoInsufficientRights","PNP_VetoLegacyDevice","PNP_VetoLegacyDriver","PNP_VetoNonDisableable","PNP_VetoOutstandingOpen","PNP_VetoPendingClose","PNP_VetoTypeUnknown","PNP_VetoWindowsApp","PNP_VetoWindowsService","PPNP_VETO_TYPE","PPNP_VETO_TYPE enumeration pointer [Device and Driver Installation]","cfg/PNP_VETO_TYPE","cfg/PNP_VetoDevice","cfg/PNP_VetoDriver","cfg/PNP_VetoIllegalDeviceRequest","cfg/PNP_VetoInsufficientPower","cfg/PNP_VetoInsufficientRights","cfg/PNP_VetoLegacyDevice","cfg/PNP_VetoLegacyDriver","cfg/PNP_VetoNonDisableable","cfg/PNP_VetoOutstandingOpen","cfg/PNP_VetoPendingClose","cfg/PNP_VetoTypeUnknown","cfg/PNP_VetoWindowsApp","cfg/PNP_VetoWindowsService","cfg/PPNP_VETO_TYPE","cfgmgrenum_8b47c6f6-4b36-472b-8389-11391558c252.xml","devinst.pnp_veto_type"]
old-location: devinst\pnp_veto_type.htm
tech.root: devinst
ms.assetid: aa999860-cabf-480e-9e17-574de169f464
ms.date: 12/05/2018
ms.keywords: '*PPNP_VETO_TYPE, PNP_VETO_TYPE, PNP_VETO_TYPE enumeration [Device and Driver Installation], PNP_VetoDevice, PNP_VetoDriver, PNP_VetoIllegalDeviceRequest, PNP_VetoInsufficientPower, PNP_VetoInsufficientRights, PNP_VetoLegacyDevice, PNP_VetoLegacyDriver, PNP_VetoNonDisableable, PNP_VetoOutstandingOpen, PNP_VetoPendingClose, PNP_VetoTypeUnknown, PNP_VetoWindowsApp, PNP_VetoWindowsService, PPNP_VETO_TYPE, PPNP_VETO_TYPE enumeration pointer [Device and Driver Installation], cfg/PNP_VETO_TYPE, cfg/PNP_VetoDevice, cfg/PNP_VetoDriver, cfg/PNP_VetoIllegalDeviceRequest, cfg/PNP_VetoInsufficientPower, cfg/PNP_VetoInsufficientRights, cfg/PNP_VetoLegacyDevice, cfg/PNP_VetoLegacyDriver, cfg/PNP_VetoNonDisableable, cfg/PNP_VetoOutstandingOpen, cfg/PNP_VetoPendingClose, cfg/PNP_VetoTypeUnknown, cfg/PNP_VetoWindowsApp, cfg/PNP_VetoWindowsService, cfg/PPNP_VETO_TYPE, cfgmgrenum_8b47c6f6-4b36-472b-8389-11391558c252.xml, devinst.pnp_veto_type'
req.header: cfg.h
req.include-header: Cfgmgr32.h
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
req.typenames: PNP_VETO_TYPE, *PPNP_VETO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PNP_VETO_TYPE
 - cfg/_PNP_VETO_TYPE
 - PPNP_VETO_TYPE
 - cfg/PPNP_VETO_TYPE
 - PNP_VETO_TYPE
 - cfg/PNP_VETO_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfg.h
api_name:
 - PNP_VETO_TYPE
---

# PNP_VETO_TYPE enumeration


## -description

If the PnP manager rejects a request to perform an operation, the PNP_VETO_TYPE enumeration is used to identify the reason for the rejection.

## -enum-fields

### -field PNP_VetoTypeUnknown

The specified operation was rejected for an unknown reason.

### -field PNP_VetoLegacyDevice

The device does not support the specified PnP operation.

### -field PNP_VetoPendingClose

The specified operation cannot be completed because of a pending close operation.

### -field PNP_VetoWindowsApp

A Microsoft Win32 application vetoed the specified operation.

### -field PNP_VetoWindowsService

A Win32 service vetoed the specified operation.

### -field PNP_VetoOutstandingOpen

The requested operation was rejected because of outstanding open handles.

### -field PNP_VetoDevice

The device supports the specified operation, but the device rejected the operation.

### -field PNP_VetoDriver

The driver supports the specified operation, but the driver rejected the operation.

### -field PNP_VetoIllegalDeviceRequest

The device does not support the specified operation.

### -field PNP_VetoInsufficientPower

There is insufficient power to perform the requested operation.

### -field PNP_VetoNonDisableable

The device cannot be disabled.

### -field PNP_VetoLegacyDriver

The driver does not support the specified PnP operation.

### -field PNP_VetoInsufficientRights

The caller has insufficient privileges to complete the operation.

## -remarks

Text strings are associated with most of the veto types, and a function that receives a veto type value can typically request to also receive the value's associated text string. The following table identifies the text string associated with each value.

<table>
<tr>
<th>pVeto type value</th>
<th>Text String</th>
</tr>
<tr>
<td>
<b>PNP_VetoTypeUnknown</b>

</td>
<td>
None.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoLegacyDevice
       </b>

</td>
<td>
A device instance path.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoPendingClose
       </b>

</td>
<td>
A device instance path.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoWindowsApp</b>

</td>
<td>
An application module name.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoWindowsService
       </b>

</td>
<td>
A Windows service name.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoOutstandingOpen
       </b>

</td>
<td>
A device instance path.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoDevice
       </b>

</td>
<td>
A device instance path.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoDriver
       </b>

</td>
<td>
A driver name.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoIllegalDeviceRequest</b>

</td>
<td>
A device instance path.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoInsufficientPower
       </b>

</td>
<td>
None.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoNonDisableable</b>

</td>
<td>
A device instance path.

</td>
</tr>
<tr>
<td>
<b>PNP_VetoLegacyDriver
       </b>

</td>
<td>
A Windows service name.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew">CM_Query_And_Remove_SubTree</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw">CM_Query_And_Remove_SubTree_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw">CM_Request_Device_Eject</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw">CM_Request_Device_Eject_Ex</a>