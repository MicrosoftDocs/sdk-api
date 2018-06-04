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

# GetIfStackTable function


## -description


The <b>GetIfStackTable</b> function  retrieves a table of network interface stack row entries that specify the relationship of the network interfaces on an interface stack.


## -parameters




### -param Table [out]

A pointer to a buffer that receives the table of interface stack row entries in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a> structure.


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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the  <i>Table</i> parameter. 

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No interface stack entries were found.

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



The <b>GetIfStackTable</b> function is defined on Windows Vista and later. 

The  
<b>GetIfStackTable</b> function enumerates the physical and logical network interfaces on an interface stack on a local system and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a> structure. 

Interface stack entries are returned in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_IFSTACK_TABLE</b> structure contains an interface stack entry count and an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff559207">MIB_IFSTACK_ROW</a> structures for each interface stack entry. 

The relationship between the interfaces in the interface stack is that the interface with index in the <b>HigherLayerInterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559207">MIB_IFSTACK_ROW</a> structure is immediately above the interface with index in the <b>LowerLayerInterfaceIndex</b> member of the <b>MIB_IFSTACK_ROW</b> structure.

Memory is allocated by the <b>GetIfStackTable</b> function for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a> structure and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559207">MIB_IFSTACK_ROW</a> entries in this structure. When these returned structures are no longer required, free the memory by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a>.

Note that the returned <a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff559207">MIB_IFSTACK_ROW</a> array entry in the <b>Table</b> member of the <b>MIB_IFSTACK_TABLE</b> structure. Padding for alignment may also be present between the <b>MIB_IFSTACK_ROW</b> array entries. Any access to a <b>MIB_IFSTACK_ROW</b> array entry should assume  padding may exist. 






## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552517">GetIfEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552524">GetIfTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552531">GetInvertedIfStackTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552540">GetIpInterfaceEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554883">InitializeIpInterfaceEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559207">MIB_IFSTACK_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559210">MIB_IFSTACK_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559234">MIB_INVERTEDIFSTACK_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559240">MIB_INVERTEDIFSTACK_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559254">MIB_IPINTERFACE_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568805">NotifyIpInterfaceChange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570774">SetIpInterfaceEntry</a>
 

 

