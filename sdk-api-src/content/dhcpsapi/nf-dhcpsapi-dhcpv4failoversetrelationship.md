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

# DhcpV4FailoverSetRelationship function


## -description


The <b>DhcpV4FailoverSetRelationship</b> function sets or modifies the parameters of a DHCPv4 server failover relationship.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param Flags

TBD


### -param pRelationship [in]

Pointer to a <a href="https://msdn.microsoft.com/b409b0ff-2fdc-416c-a7ce-2cba9cf75122">DHCP_FAILOVER_RELATIONSHIP</a> structure that  contains  update information about the fields in the DHCPv4 failover relationship.


#### - flags [in]

A bitmask that specifies the fields to update in <i>pRelationship</i>. Each value specifies a member of the <a href="https://msdn.microsoft.com/b409b0ff-2fdc-416c-a7ce-2cba9cf75122">DHCP_FAILOVER_RELATIONSHIP</a> structure to be modified. 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCLT"></a><a id="mclt"></a><dl>
<dt><b>MCLT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>mclt</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFEPERIOD"></a><a id="safeperiod"></a><dl>
<dt><b>SAFEPERIOD</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>safePeriod</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGESTATE"></a><a id="changestate"></a><dl>
<dt><b>CHANGESTATE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <b>state</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="PERCENTAGE"></a><a id="percentage"></a><dl>
<dt><b>PERCENTAGE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The <b>percentage</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="MODE"></a><a id="mode"></a><dl>
<dt><b>MODE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The <b>mode</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="PREVSTATE"></a><a id="prevstate"></a><dl>
<dt><b>PREVSTATE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The <b>prevState</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_RELATIONSHIP_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The failover relationship doesn’t exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6e360dd4-b4a0-4652-8754-17c3c284271c">DhcpV4FailoverCreateRelationship</a>



<a href="https://msdn.microsoft.com/c7b894a4-4def-41fe-98b6-f56d6ff0c715">DhcpV4FailoverDeleteRelationship</a>



<a href="https://msdn.microsoft.com/81ef2af8-c1a9-44e7-857c-1591947609ed">DhcpV4FailoverEnumRelationship</a>



<a href="https://msdn.microsoft.com/b637d1e8-8c61-4382-a5ec-3d5395433f86">DhcpV4FailoverGetRelationship</a>
 

 

