---
UID: NS:mprapi._MPR_SERVER_2
title: MPR_SERVER_2 (mprapi.h)
description: Is used to retrieve and set the number of ports available for the Point-to-Point Tunneling Protocol (PPTP), Layer 2 Tunneling Protocol (L2TP), and Secure Socket Tunneling Protocol (SSTP) on a device.
helpviewer_keywords: ["*PMPR_SERVER_2","MPR_ENABLE_RAS_ON_DEVICE","MPR_ENABLE_ROUTING_ON_DEVICE","MPR_SERVER_2","MPR_SERVER_2 structure [RAS]","PMPR_SERVER_2","PMPR_SERVER_2 structure pointer [RAS]","mprapi/MPR_SERVER_2","mprapi/PMPR_SERVER_2","rras.mpr_server_2"]
old-location: rras\mpr_server_2.htm
tech.root: RRAS
ms.assetid: 9e38651a-541f-4470-a841-4eb94dbe4835
ms.date: 12/05/2018
ms.keywords: '*PMPR_SERVER_2, MPR_ENABLE_RAS_ON_DEVICE, MPR_ENABLE_ROUTING_ON_DEVICE, MPR_SERVER_2, MPR_SERVER_2 structure [RAS], PMPR_SERVER_2, PMPR_SERVER_2 structure pointer [RAS], mprapi/MPR_SERVER_2, mprapi/PMPR_SERVER_2, rras.mpr_server_2'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MPR_SERVER_2, *PMPR_SERVER_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_SERVER_2
 - mprapi/_MPR_SERVER_2
 - PMPR_SERVER_2
 - mprapi/PMPR_SERVER_2
 - MPR_SERVER_2
 - mprapi/MPR_SERVER_2
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
 - MPR_SERVER_2
---

# MPR_SERVER_2 structure


## -description

The <b>MPR_SERVER_2</b> structure is used to retrieve and set the number of ports available for the Point-to-Point Tunneling Protocol (PPTP), Layer 2 Tunneling Protocol (L2TP), and Secure Socket Tunneling Protocol (SSTP) on a device.

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
Windows Web Server 2008

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Standard

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>16,384</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Datacenter and Windows Server 2008 Enterprise

</td>
</tr>
</table>
 

If <i>dwNumPptpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a> and <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.

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
Windows Web Server 2008

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Standard

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>30,000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Datacenter and Windows Server 2008 Enterprise

</td>
</tr>
</table>
 

If <i>dwNumL2tpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a> and <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.

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

### -field dwNumSstpPorts

Specifies the number of ports configured for SSTP on the device. 
 The maximum values for <i>dwNumSstpPorts</i> are listed in the following table. The value zero is not allowed.

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
Windows Web Server 2008

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Standard

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>30,000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Datacenter and Windows Server 2008 Enterprise

</td>
</tr>
</table>
 

If <i>dwNumSstpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a> and <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.

### -field dwSstpPortFlags

A set of bitflags that indicate if RAS is enabled on the device.

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
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfo">MprAdminServerGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigservergetinfo">MprConfigServerGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>