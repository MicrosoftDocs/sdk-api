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

# Tbsi_Physical_Presence_Command function


## -description


Passes a physical presence ACPI command through TBS to the driver.


## -parameters




### -param hContext [in]

The context of the ACPI command.


### -param pabInput [in]

A pointer to a buffer that contains the input to the ACPI command.


The input to the ACPI command is defined in the <a href="https://go.microsoft.com/fwlink/p/?linkid=148313">TCG Physical Presence Interface Specification</a> at https://www.trustedcomputinggroup.org/specs/PCClient. The buffer should contain <i>Arg2</i> and <i>Arg3</i> values as defined in this document. The values for <i>Arg0</i> and <i>Arg1</i> are static and automatically added. For example, if this method is used for Get Physical Presence Interface Version, then <i>Arg2</i> is the integer value 1 and <i>Arg3</i> is empty, so the buffer should just contain an integer value of 1. If this method is used for "Submit TPM Operation Request to Pre-OS Environment", then <i>Arg2</i> is the integer value 2 and <i>Arg3</i> will be the integer for the specified operation, such as 1 for enable or 2 for disable.


### -param cbInput [in]

The length, in bytes, of the input buffer.


### -param pabOutput [out]

A pointer to a buffer to contain the output of the ACPI command.


The buffer will contain the return value from the  command as defined in the <a href="https://go.microsoft.com/fwlink/p/?linkid=148313">TCG Physical Presence Interface Specification</a>.


### -param pcbOutput [in, out]

A pointer to an unsigned long integer that, on input, specifies the size, in bytes, of the output buffer. If the function succeeds, this parameter, on output, receives the size, in bytes, of the data pointed to by <i>pabOutput</i>. If the function fails, this parameter does not receive a value.


## -returns



If the function succeeds, the function returns TBS_SUCCESS.

If the function fails, it returns a TBS return code that indicates the error.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_BAD_PARAMETER</b></dt>
<dt>2150121474 (0x80284002)</dt>
</dl>
</td>
<td width="60%">
One or more parameter values are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INTERNAL_ERROR</b></dt>
<dt>2150121473 (0x80284001)</dt>
</dl>
</td>
<td width="60%">
An internal software error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_CONTEXT_PARAM</b></dt>
<dt>2150121479 (0x80284007)</dt>
</dl>
</td>
<td width="60%">
A context parameter that is not valid was passed when attempting to create a TBS context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_OUTPUT_POINTER</b></dt>
<dt>2150121475 (0x80284003)</dt>
</dl>
</td>
<td width="60%">
A specified output pointer is not valid.

</td>
</tr>
</table>
 




## -remarks



For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=148313">TCG Physical Presence Interface Specification</a>.



