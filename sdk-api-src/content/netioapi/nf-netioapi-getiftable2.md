---
UID: NF:netioapi.GetIfTable2
title: GetIfTable2 function
author: windows-sdk-content
description: Retrieves the MIB-II interface table.
old-location: iphlp\getiftable2.htm
tech.root: IpHlp
ms.assetid: 0153c41c-b02b-4832-87b3-88dc3a9f4ff1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetIfTable2, GetIfTable2 function [IP Helper], iphlp.getiftable2, netioapi/GetIfTable2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIfTable2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIfTable2 function


## -description


The <b>GetIfTable2</b> function  retrieves the MIB-II interface table.


## -parameters




### -param Table [out]

A pointer to a buffer that receives the table of interfaces in a <a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a> structure.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory resources are available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The  
<b>GetIfTable2</b> function enumerates the logical and physical interfaces on a local system and returns this information in a <a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a> structure. <b>GetIfTable2</b> is an enhanced version of the <b>GetIfTable</b> function. 

A similar <a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a> function can be used to specify the level of interfaces to return. Calling the <b>GetIfTable2Ex</b> function with the <i>Level</i> parameter set to <b>MibIfTableNormal</b> retrieves the same results as calling the <b>GetIfTable2</b> function.

Interfaces are returned in a <a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_IF_TABLE2</b> structure contains an interface count and an array of <a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a> structures for each interface. Memory is allocated by the <b>GetIfTable2</b> function for the <b>MIB_IF_TABLE2</b> structure and the <b>MIB_IF_ROW2</b> entries in this structure. When these returned structures are no longer required, free the memory by calling the <a href="https://msdn.microsoft.com/31c8cdc4-73c7-4e82-8226-c90320046199">FreeMibTable</a>.

Note that the returned <a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a> array entry in the <b>Table</b> member of the <b>MIB_IF_TABLE2</b> structure. Padding for alignment may also be present between the <b>MIB_IF_ROW2</b> array entries. Any access to a <b>MIB_IF_ROW2</b> array entry should assume  padding may exist. 






## -see-also




<a href="https://msdn.microsoft.com/31c8cdc4-73c7-4e82-8226-c90320046199">FreeMibTable</a>



<a href="https://msdn.microsoft.com/6a46c1df-b274-415e-b842-fc1adf6fa206">GetIfTable</a>



<a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a>
 

 

