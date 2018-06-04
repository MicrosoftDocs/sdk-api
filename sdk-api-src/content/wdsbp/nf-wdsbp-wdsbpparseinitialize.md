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

# WdsBpParseInitialize function


## -description


Receives a handle to the packet sent by the network boot program.


## -parameters




### -param pPacket [in]

A pointer to the packet received from the WDS client. The packet must be a valid DHCP packet.


### -param uPacketLen [in]

The length of the packet, in bytes.


### -param pbPacketType [out, optional]

A value that indicates the type of boot program that sent the packet. The bit flags in the following table can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_DHCP"></a><a id="wdsbp_pk_type_dhcp"></a><dl>
<dt><b>WDSBP_PK_TYPE_DHCP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The presence of this value indicates that the packet is a DHCP packet.

</td>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_WDSNBP"></a><a id="wdsbp_pk_type_wdsnbp"></a><dl>
<dt><b>WDSBP_PK_TYPE_WDSNBP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
This presence of this value indicates that the DHCP packet came from the WDS network boot program. If this value is absent the type of client was not recognized.

</td>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_BCD"></a><a id="wdsbp_pk_type_bcd"></a><dl>
<dt><b>WDSBP_PK_TYPE_BCD</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The presence of this value indicates that the packet contains a path to a Boot Configuration Data (BCD) file. 

</td>
</tr>
</table>
 


### -param phHandle [out]

A handle to the packet. This handle can be used by the <a href="https://msdn.microsoft.com/98c0d220-db20-4aba-9df0-e50f3b947da2">WdsBpQueryOption</a> function and must be closed using the <a href="https://msdn.microsoft.com/b35ec3e2-7dd5-4e17-b657-72bafe91921a">WdsBpCloseHandle</a> function.


## -returns



If the function succeeds, the return is <b>S_OK</b>.



