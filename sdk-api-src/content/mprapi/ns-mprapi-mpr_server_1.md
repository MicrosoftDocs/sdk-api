---
UID: NS:mprapi._MPR_SERVER_1
title: MPR_SERVER_1 (mprapi.h)
description: Is used to retrieve and set the number of ports available for the Point-to-Point Tunneling Protocol (PPTP) and Layer 2 Tunneling Protocol (L2TP) on a device.
helpviewer_keywords: ["*PMPR_SERVER_1","MPR_ENABLE_RAS_ON_DEVICE","MPR_ENABLE_ROUTING_ON_DEVICE","MPR_SERVER_1","MPR_SERVER_1 structure [RAS]","PMPR_SERVER_1","PMPR_SERVER_1 structure pointer [RAS]","mprapi/MPR_SERVER_1","mprapi/PMPR_SERVER_1","rras.mpr_server_1"]
old-location: rras\mpr_server_1.htm
tech.root: RRAS
ms.assetid: ea27a928-055b-4705-8f7c-dd9a221b2573
ms.date: 12/05/2018
ms.keywords: '*PMPR_SERVER_1, MPR_ENABLE_RAS_ON_DEVICE, MPR_ENABLE_ROUTING_ON_DEVICE, MPR_SERVER_1, MPR_SERVER_1 structure [RAS], PMPR_SERVER_1, PMPR_SERVER_1 structure pointer [RAS], mprapi/MPR_SERVER_1, mprapi/PMPR_SERVER_1, rras.mpr_server_1'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
targetos: Windows
req.typenames: MPR_SERVER_1, *PMPR_SERVER_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_SERVER_1
 - mprapi/_MPR_SERVER_1
 - PMPR_SERVER_1
 - mprapi/PMPR_SERVER_1
 - MPR_SERVER_1
 - mprapi/MPR_SERVER_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_SERVER_1
---

# MPR_SERVER_1 structure


## -description

The <b>MPR_SERVER_1</b> structure is used to retrieve and set the number of ports available for the Point-to-Point Tunneling Protocol (PPTP) and Layer 2 Tunneling Protocol (L2TP) on a device.

## -struct-fields

### -field dwNumPptpPorts

Specifies the number of ports configured for PPTP on the device. 
The maximum values for <i>dwNumPptpPorts</i> are listed in the following table. The value zero is not allowed.

<table>
<tr>
<th>Maximum Value</th>
<th>Windows Version</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Web Edition

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Standard Edition

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>16,384</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Datacenter Edition and Windows Server 2003, Enterprise Edition

</td>
</tr>
</table>
 

If <i>dwNumPptpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2003, Standard Edition and Windows Server 2003, Enterprise Edition), the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a> and <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.

### -field dwPptpPortFlags

A set of bitflags that indicate if RAS or Routing is enabled on the device.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPR_ENABLE_RAS_ON_DEVICE"></a><a id="mpr_enable_ras_on_device"></a><dl>
<dt><b>MPR_ENABLE_RAS_ON_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, RAS is enabled on the device.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_ENABLE_ROUTING_ON_DEVICE"></a><a id="mpr_enable_routing_on_device"></a><dl>
<dt><b>MPR_ENABLE_ROUTING_ON_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, Routing is enabled on the device.

</td>
</tr>
</table>

### -field dwNumL2tpPorts

Specifies the number of ports configured for L2TP on the device. 
The maximum values for <i>dwNumL2tpPorts</i> are listed in the following table. The value zero is not allowed.

<table>
<tr>
<th>Maximum Value</th>
<th>Windows Version</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Web Edition

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Standard Edition

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>30,000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Datacenter Edition and Windows Server 2003, Enterprise Edition

</td>
</tr>
</table>
 

If <i>dwNumL2tpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2003, Standard Edition and Windows Server 2003, Enterprise Edition), the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a> and <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.

### -field dwL2tpPortFlags

A set of bitflags that indicate if RAS or Routing is enabled on the device.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPR_ENABLE_RAS_ON_DEVICE"></a><a id="mpr_enable_ras_on_device"></a><dl>
<dt><b>MPR_ENABLE_RAS_ON_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, RAS is enabled on the device.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_ENABLE_ROUTING_ON_DEVICE"></a><a id="mpr_enable_routing_on_device"></a><dl>
<dt><b>MPR_ENABLE_ROUTING_ON_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, Routing is enabled on the device.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfo">MprAdminServerGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigservergetinfo">MprConfigServerGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>