---
UID: NS:mprapi._MPR_SERVER_2
title: "_MPR_SERVER_2"
author: windows-sdk-content
description: Is used to retrieve and set the number of ports available for the Point-to-Point Tunneling Protocol (PPTP), Layer 2 Tunneling Protocol (L2TP), and Secure Socket Tunneling Protocol (SSTP) on a device.
old-location: rras\mpr_server_2.htm
old-project: RRAS
ms.assetid: 9e38651a-541f-4470-a841-4eb94dbe4835
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PMPR_SERVER_2, MPR_ENABLE_RAS_ON_DEVICE, MPR_ENABLE_ROUTING_ON_DEVICE, MPR_SERVER_2, MPR_SERVER_2 structure [RAS], PMPR_SERVER_2, PMPR_SERVER_2 structure pointer [RAS], _MPR_SERVER_2, mprapi/MPR_SERVER_2, mprapi/PMPR_SERVER_2, rras.mpr_server_2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MPR_SERVER_2, *PMPR_SERVER_2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_SERVER_2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MPR_SERVER_2 structure


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
 

If <i>dwNumPptpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="https://msdn.microsoft.com/95fe0dfb-cfa6-4e84-a060-4b0fffc71a3d">MprConfigServerSetInfo</a> and <a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.


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
 

If <i>dwNumL2tpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="https://msdn.microsoft.com/95fe0dfb-cfa6-4e84-a060-4b0fffc71a3d">MprConfigServerSetInfo</a> and <a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.


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
 

If <i>dwNumSstpPorts</i> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="https://msdn.microsoft.com/95fe0dfb-cfa6-4e84-a060-4b0fffc71a3d">MprConfigServerSetInfo</a> and <a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminServerSetInfo</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.


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




<a href="https://msdn.microsoft.com/cffda25b-28f8-4d76-987c-eadcea9c032b">MPR_SERVER_0</a>



<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>



<a href="https://msdn.microsoft.com/d15dfb60-1239-4552-985f-d3c98f2981f4">MprAdminServerGetInfo</a>



<a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminServerSetInfo</a>



<a href="https://msdn.microsoft.com/6d3cd97a-96ef-4ecd-b2fd-2743ba79aa5b">MprConfigServerGetInfo</a>



<a href="https://msdn.microsoft.com/95fe0dfb-cfa6-4e84-a060-4b0fffc71a3d">MprConfigServerSetInfo</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

