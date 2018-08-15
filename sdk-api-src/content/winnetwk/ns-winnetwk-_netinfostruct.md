---
UID: NS:winnetwk._NETINFOSTRUCT
title: "_NETINFOSTRUCT"
author: windows-sdk-content
description: Contains information describing the network provider returned by the WNetGetNetworkInformation function.
old-location: wnet\netinfostruct_str.htm
old-project: wnet
ms.assetid: 2f60209f-7777-4130-b212-245673dd0055
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPNETINFOSTRUCT, ERROR_BUSY, ERROR_NO_NETWORK, LPNETINFOSTRUCT, LPNETINFOSTRUCT structure pointer [Windows Networking (WNet)], NETINFOSTRUCT, NETINFOSTRUCT structure [Windows Networking (WNet)], NETINFO_DISKRED, NETINFO_DLL16, NETINFO_PRINTERRED, NO_ERROR, _NETINFOSTRUCT, _win32_netinfostruct_str, winnetwk/LPNETINFOSTRUCT, winnetwk/NETINFOSTRUCT, wnet.netinfostruct_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnetwk.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: NETINFOSTRUCT, *LPNETINFOSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - NETINFOSTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _NETINFOSTRUCT structure


## -description


The
				<b>NETINFOSTRUCT</b> structure contains information describing the network provider returned by the 
<a href="https://msdn.microsoft.com/df190133-b73b-4f3e-aaee-4095cd619065">WNetGetNetworkInformation</a> function.


## -struct-fields




### -field cbStructure

Type: <b>DWORD</b>

The size, in bytes, of the 
<b>NETINFOSTRUCT</b> structure. The caller must supply this value to indicate the size of the structure passed in. Upon return, it has the size of the structure filled in.


### -field dwProviderVersion

Type: <b>DWORD</b>

The version number of the network provider software.


### -field dwStatus

Type: <b>DWORD</b>

The current status of the network provider software. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NO_ERROR"></a><a id="no_error"></a><dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The network is running.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_NO_NETWORK"></a><a id="error_no_network"></a><dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_BUSY"></a><a id="error_busy"></a><dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The network is not currently able to service requests, but it should become available shortly. (This value typically indicates that the network is starting up.)

</td>
</tr>
</table>
 


### -field dwCharacteristics

Type: <b>DWORD</b>

Characteristics of the network provider software. 


This value is zero.

<b>Windows Me/98/95:  </b>This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETINFO_DLL16"></a><a id="netinfo_dll16"></a><dl>
<dt><b>NETINFO_DLL16</b></dt>
</dl>
</td>
<td width="60%">
The network provider is running as a 16-bit Windows network driver.

</td>
</tr>
<tr>
<td width="40%"><a id="NETINFO_DISKRED"></a><a id="netinfo_diskred"></a><dl>
<dt><b>NETINFO_DISKRED</b></dt>
</dl>
</td>
<td width="60%">
The network provider requires a redirected local disk drive device to access server file systems.

</td>
</tr>
<tr>
<td width="40%"><a id="NETINFO_PRINTERRED"></a><a id="netinfo_printerred"></a><dl>
<dt><b>NETINFO_PRINTERRED</b></dt>
</dl>
</td>
<td width="60%">
The network provider requires a redirected local printer port to access server file systems.

</td>
</tr>
</table>
 


### -field dwHandle

Type: <b>ULONG_PTR</b>

An instance handle for the network provider or for the 16-bit Windows network driver.


### -field wNetType

Type: <b>WORD</b>

The network type unique to the running network. This value associates resources with a specific network when the resources are persistent or stored in links. You can find a complete list of network types in the header file Winnetwk.h.


### -field dwPrinters

Type: <b>DWORD</b>

A set of bit flags indicating the valid print numbers for redirecting local printer devices, with the low-order bit corresponding to LPT1. 




<b>Windows Me/98/95:  </b>This value is always set to –1.


### -field dwDrives

Type: <b>DWORD</b>

A set of bit flags indicating the valid local disk devices for redirecting disk drives, with the low-order bit corresponding to A:. 




<b>Windows Me/98/95:  </b>This value is always set to –1.


## -remarks



The <b>NETINFOSTRUCT</b> structure contains information describing the network, such as the version of the network provider software and the network's current status.




## -see-also




<a href="https://msdn.microsoft.com/df190133-b73b-4f3e-aaee-4095cd619065">WNetGetNetworkInformation</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/7969ccbb-d1ae-4a1f-8b9c-862cc6ddef1a">Windows Networking Structures</a>
 

 

