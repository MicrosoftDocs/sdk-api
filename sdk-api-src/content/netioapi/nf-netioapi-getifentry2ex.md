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

# GetIfEntry2Ex function


## -description


The 
<b>GetIfEntry2Ex</b> function  retrieves the specified level of information for the specified interface on the local computer.


## -parameters




### -param Level [in]

The level of interface information to retrieve. This parameter can be one of the values from the <b>MIB_IF_ENTRY_LEVEL</b> enumeration type defined in the <i>Netioapi.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MibIfEntryNormal"></a><a id="mibifentrynormal"></a><a id="MIBIFENTRYNORMAL"></a><dl>
<dt><b>MibIfEntryNormal</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The values of statistics and state returned in members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure pointed to by the <i>Row</i> parameter are returned from the top of the filter stack.

</td>
</tr>
<tr>
<td width="40%"><a id="MibIfEntryNormalWithoutStatistics_"></a><a id="mibifentrynormalwithoutstatistics_"></a><a id="MIBIFENTRYNORMALWITHOUTSTATISTICS_"></a><dl>
<dt><b>MibIfEntryNormalWithoutStatistics </b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The values of state (without statistics) returned in members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure  pointed to by the <i>Row</i> parameter are returned from the top of the filter stack.

</td>
</tr>
</table>
 


### -param Row [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure that, on successful return, receives information for an interface on the local computer. On input, the <b>InterfaceLuid</b> or the <b>InterfaceIndex</b> member of the <b>MIB_IF_ROW2</b> must be set to the interface for which to retrieve information.


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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> pointed to by the <i>Row</i> parameter was not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> parameter is passed in the <i>Row</i> parameter. This error is also returned if the both the <b>InterfaceLuid</b> and <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> pointed to by the <i>Row</i> parameter  are unspecified.

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
the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The  
<b>GetIfEntry2Ex</b> function retrieves information for a specified interface on a local system and returns this information in a pointer to a  
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure. <b>GetIfEntry2Ex</b> is an enhanced version of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552517">GetIfEntry2</a> function that allows selecting the level of interface information to retrieve.

On input, at least one of the following members in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure passed in the <i>Row</i> parameter must be initialized:
    <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the value of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output, the remaining fields of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure pointed to by the <i>Row</i> parameter are filled in.

Note that the <i>Netioapi.h</i> header file is automatically included in <i>Iphlpapi.h</i> header file, and should never be used directly.





## -see-also




<b>GetIfEntry</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552517">GetIfEntry2</a>



<a href="https://msdn.microsoft.com/6a46c1df-b274-415e-b842-fc1adf6fa206">GetIfTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552524">GetIfTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a>



<a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a>
 

 

