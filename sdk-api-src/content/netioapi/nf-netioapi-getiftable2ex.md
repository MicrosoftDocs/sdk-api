---
UID: NF:netioapi.GetIfTable2Ex
title: GetIfTable2Ex function
author: windows-sdk-content
description: Retrieves the MIB-II interface table.
old-location: iphlp\getiftable2ex.htm
old-project: iphlp
ms.assetid: d8663894-50b1-4ca2-a1f4-6ca0970795a7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetIfTable2Ex, GetIfTable2Ex function [IP Helper], MibIfTableNormal, MibIfTableRaw, iphlp.getiftable2ex, netioapi/GetIfTable2Ex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIfTable2Ex
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetIfTable2Ex function


## -description


The <b>GetIfTable2Ex</b> function  retrieves the MIB-II interface table.


## -parameters




### -param Level [in]

The level of interface information to retrieve. This parameter can be one of the values from the <b>MIB_IF_TABLE_LEVEL</b> enumeration type defined in the <i>Netioapi.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MibIfTableNormal"></a><a id="mibiftablenormal"></a><a id="MIBIFTABLENORMAL"></a><dl>
<dt><b>MibIfTableNormal</b></dt>
</dl>
</td>
<td width="60%">
The values of statistics and state returned in members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure pointed to by the <i>Table</i> parameter are returned from the top of the filter stack when this parameter is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MibIfTableRaw"></a><a id="mibiftableraw"></a><a id="MIBIFTABLERAW"></a><dl>
<dt><b>MibIfTableRaw</b></dt>
</dl>
</td>
<td width="60%">
The values of statistics and state returned in members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure pointed to by the <i>Table</i> parameter are returned directly for the interface being queried.

</td>
</tr>
</table>
 


### -param Table [out]

A pointer to a buffer that receives the table of interfaces in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if an illegal value was passed in the <i>Level</i> parameter.

</td>
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
<b>GetIfTable2Ex</b> function enumerates the logical and physical interfaces on a local system and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure. <b>GetIfTable2Ex</b> is an enhanced version of the <b>GetIfTable</b> function that allows selecting the level of interface information to retrieve.

A similar <a href="https://msdn.microsoft.com/library/windows/hardware/ff552524">GetIfTable2</a> function can also be used to retrieve interfaces. but does not allow specifying the level of interfaces  to return. Calling the <b>GetIfTable2Ex</b> function with the <i>Level</i> parameter set to <b>MibIfTableNormal</b> retrieves the same results as calling the <b>GetIfTable2</b> function.

Interfaces are returned in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_IF_TABLE2</b> structure contains an interface count and an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structures for each interface. Memory is allocated by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552524">GetIfTable2</a> function for the <b>MIB_IF_TABLE2</b> structure and the <b>MIB_IF_ROW2</b> entries in this structure. When these returned structures are no longer required, free the memory by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a>.

All interfaces including NDIS intermediate driver interfaces and NDIS filter driver interfaces are returned for either of the possible values for the <i>Level</i> parameter. The setting for the <i>Level</i> parameter affects how statistics and state members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure pointed to by the <i>Table</i> parameter for the interface are returned. For example, a network interface card (NIC)  will have a NDIS miniport driver.  An NDIS intermediate driver can be installed to  interface between upper-level protocol drivers and NDIS miniport drivers. An NDIS filter driver (LWF) can be attached on top of the NDIS intermediate driver. Assume that the NIC reports the MediaConnectState member of the  <b>MIB_IF_ROW2</b> structure as <b>MediaConnectStateConnected</b>but NDIS filter driver modifies the state and reports the state as <b>MediaConnectStateDisconnected</b>.
When the interface information is queried with <i>Level</i> parameter set to <b>MibIfTableNormal</b>, the state at the top of the filter stack, that is <b>MediaConnectStateDisconnected</b> is reported. When the interface is queried with the <i>Level</i> parameter set to <b>MibIfTableRaw</b>, the state at the interface level directly, that is <b>MediaConnectStateConnected</b> is returned.


Note that the returned <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> array entry in the <b>Table</b> member of the <b>MIB_IF_TABLE2</b> structure. Padding for alignment may also be present between the <b>MIB_IF_ROW2</b> array entries. Any access to a <b>MIB_IF_ROW2</b> array entry should assume  padding may exist. 






## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a>



<a href="https://msdn.microsoft.com/6a46c1df-b274-415e-b842-fc1adf6fa206">GetIfTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552524">GetIfTable2</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a>
 

 

