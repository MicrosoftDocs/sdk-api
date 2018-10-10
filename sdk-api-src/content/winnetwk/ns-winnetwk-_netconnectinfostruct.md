---
UID: NS:winnetwk._NETCONNECTINFOSTRUCT
title: "_NETCONNECTINFOSTRUCT"
author: windows-sdk-content
description: Contains information about the expected performance of a connection used to access a network resource.
old-location: wnet\netconnectinfostruct_str.htm
tech.root: WNet
ms.assetid: 977c717d-7624-46ab-b17d-25f42ef68be8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPNETCONNECTINFOSTRUCT, LPNETCONNECTINFOSTRUCT, LPNETCONNECTINFOSTRUCT structure pointer [Windows Networking (WNet)], NETCONNECTINFOSTRUCT, NETCONNECTINFOSTRUCT structure [Windows Networking (WNet)], WNCON_DYNAMIC, WNCON_FORNETCARD, WNCON_NOTROUTED, WNCON_SLOWLINK, _NETCONNECTINFOSTRUCT, _win32_netconnectinfostruct_str, winnetwk/LPNETCONNECTINFOSTRUCT, winnetwk/NETCONNECTINFOSTRUCT, wnet.netconnectinfostruct_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnetwk.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - NETCONNECTINFOSTRUCT
product: Windows
targetos: Windows
req.typenames: NETCONNECTINFOSTRUCT, *LPNETCONNECTINFOSTRUCT
req.redist: 
---

# _NETCONNECTINFOSTRUCT structure


## -description


The
				<b>NETCONNECTINFOSTRUCT</b> structure contains information about the expected performance of a connection used to access a network resource. The information is returned by the 
<a href="https://msdn.microsoft.com/3ec4a397-e0d4-419c-9e12-6d76a87b1ca0">MultinetGetConnectionPerformance</a> function.


## -struct-fields




### -field cbStructure

Type: <b>DWORD</b>

The size, in bytes, of the 
<b>NETCONNECTINFOSTRUCT</b> structure. The caller must supply this value.


### -field dwFlags

Type: <b>DWORD</b>

A set of bit flags describing the connection. This member can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNCON_FORNETCARD"></a><a id="wncon_fornetcard"></a><dl>
<dt><b>WNCON_FORNETCARD</b></dt>
</dl>
</td>
<td width="60%">
In the absence of information about the actual connection, the information returned applies to the performance of the network card. 




If this flag is not set, information is being returned for the current connection with the resource, with any routing degradation taken into consideration.

</td>
</tr>
<tr>
<td width="40%"><a id="WNCON_NOTROUTED"></a><a id="wncon_notrouted"></a><dl>
<dt><b>WNCON_NOTROUTED</b></dt>
</dl>
</td>
<td width="60%">
The connection is not being routed. 




If this flag is not set, the connection may be going through routers that limit performance. Consequently, if WNCON_FORNETCARD is set, actual performance may be much less than the information returned.

</td>
</tr>
<tr>
<td width="40%"><a id="WNCON_SLOWLINK"></a><a id="wncon_slowlink"></a><dl>
<dt><b>WNCON_SLOWLINK</b></dt>
</dl>
</td>
<td width="60%">
The connection is over a medium that is typically slow (for example, over a modem using a normal quality phone line). You should not set the WNCON_SLOWLINK bit if the <b>dwSpeed</b> member is set to a nonzero value.

</td>
</tr>
<tr>
<td width="40%"><a id="WNCON_DYNAMIC"></a><a id="wncon_dynamic"></a><dl>
<dt><b>WNCON_DYNAMIC</b></dt>
</dl>
</td>
<td width="60%">
Some of the information returned is calculated dynamically, so reissuing this request may return different (and more current) information.

</td>
</tr>
</table>
 


### -field dwSpeed

Type: <b>DWORD</b>

Speed of the media to the network resource, in  100 bits-per-second (bps). 




For example, a 1200 baud point-to-point link returns 12. A value of zero indicates that no information is available. A value of one indicates that the actual value is greater than the maximum that can be represented by the member.


### -field dwDelay

Type: <b>DWORD</b>

One-way delay time that the network introduces when sending information, in milliseconds. (The delay is the time between when the network begins sending data and the time that the data starts being received.) This delay is in addition to any latency incorporated in the calculation of the <b>dwSpeed</b> member; therefore the value of this member is zero for most resources. 




A value of zero indicates that no information is available. A value of one indicates that the actual value is greater than the maximum that can be represented by the member.


### -field dwOptDataSize

Type: <b>DWORD</b>

Size of data that an application should use when making a single request to the network resource, in bytes. 




For example, for a disk network resource, this value might be 2048 or 512 when writing a block of data. A value of zero indicates that no information is available.


## -remarks



 The <b>NETCONNECTINFOSTRUCT</b> structure is used in the 
<a href="https://msdn.microsoft.com/3ec4a397-e0d4-419c-9e12-6d76a87b1ca0">MultinetGetConnectionPerformance</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3ec4a397-e0d4-419c-9e12-6d76a87b1ca0">MultinetGetConnectionPerformance</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/7969ccbb-d1ae-4a1f-8b9c-862cc6ddef1a">Windows Networking Structures</a>
 

 

