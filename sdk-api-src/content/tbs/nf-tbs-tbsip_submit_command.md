---
UID: NF:tbs.Tbsip_Submit_Command
title: Tbsip_Submit_Command function (tbs.h)
description: Submits a Trusted Platform Module (TPM) command to TPM Base Services (TBS) for processing.
helpviewer_keywords: ["TBS_COMMAND_LOCALITY_FOUR","TBS_COMMAND_LOCALITY_ONE","TBS_COMMAND_LOCALITY_THREE","TBS_COMMAND_LOCALITY_TWO","TBS_COMMAND_LOCALITY_ZERO","TBS_COMMAND_PRIORITY_HIGH","TBS_COMMAND_PRIORITY_LOW","TBS_COMMAND_PRIORITY_MAX","TBS_COMMAND_PRIORITY_NORMAL","TBS_COMMAND_PRIORITY_SYSTEM","Tbsip_Submit_Command","Tbsip_Submit_Command function [TBS]","tbs._tbsip_submit_command","tbs/Tbsip_Submit_Command"]
old-location: tbs\_tbsip_submit_command.htm
tech.root: TBS
ms.assetid: 5d443684-b624-47dc-abaa-a7aed74ef6cc
ms.date: 12/05/2018
ms.keywords: TBS_COMMAND_LOCALITY_FOUR, TBS_COMMAND_LOCALITY_ONE, TBS_COMMAND_LOCALITY_THREE, TBS_COMMAND_LOCALITY_TWO, TBS_COMMAND_LOCALITY_ZERO, TBS_COMMAND_PRIORITY_HIGH, TBS_COMMAND_PRIORITY_LOW, TBS_COMMAND_PRIORITY_MAX, TBS_COMMAND_PRIORITY_NORMAL, TBS_COMMAND_PRIORITY_SYSTEM, Tbsip_Submit_Command, Tbsip_Submit_Command function [TBS], tbs._tbsip_submit_command, tbs/Tbsip_Submit_Command
req.header: tbs.h
req.include-header: 
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
req.lib: Tbs.lib
req.dll: Tbs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Tbsip_Submit_Command
 - tbs/Tbsip_Submit_Command
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tbs.dll
api_name:
 - Tbsip_Submit_Command
---

# Tbsip_Submit_Command function


## -description

Submits a Trusted Platform Module (TPM) command to TPM Base Services (TBS) for processing.

## -parameters

### -param hContext [in]

The handle of the context that is submitting the command.

### -param Locality [in]

Used to set the locality for the TPM command. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_LOCALITY_ZERO"></a><a id="tbs_command_locality_zero"></a><dl>
<dt><b>TBS_COMMAND_LOCALITY_ZERO</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
Locality zero. This is the only locality currently supported.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_LOCALITY_ONE"></a><a id="tbs_command_locality_one"></a><dl>
<dt><b>TBS_COMMAND_LOCALITY_ONE</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Locality one.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_LOCALITY_TWO"></a><a id="tbs_command_locality_two"></a><dl>
<dt><b>TBS_COMMAND_LOCALITY_TWO</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Locality two.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_LOCALITY_THREE"></a><a id="tbs_command_locality_three"></a><dl>
<dt><b>TBS_COMMAND_LOCALITY_THREE</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
Locality three.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_LOCALITY_FOUR"></a><a id="tbs_command_locality_four"></a><dl>
<dt><b>TBS_COMMAND_LOCALITY_FOUR</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
Locality four.

</td>
</tr>
</table>

### -param Priority [in]

The priority level that the command should have. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_PRIORITY_LOW"></a><a id="tbs_command_priority_low"></a><dl>
<dt><b>TBS_COMMAND_PRIORITY_LOW</b></dt>
<dt>100 (0x64)</dt>
</dl>
</td>
<td width="60%">
Used for low priority application use.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_PRIORITY_NORMAL"></a><a id="tbs_command_priority_normal"></a><dl>
<dt><b>TBS_COMMAND_PRIORITY_NORMAL</b></dt>
<dt>200 (0xC8)</dt>
</dl>
</td>
<td width="60%">
Used for normal priority application use.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_PRIORITY_SYSTEM"></a><a id="tbs_command_priority_system"></a><dl>
<dt><b>TBS_COMMAND_PRIORITY_SYSTEM</b></dt>
<dt>400 (0x190)</dt>
</dl>
</td>
<td width="60%">
Used for system tasks that access the TPM.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_PRIORITY_HIGH"></a><a id="tbs_command_priority_high"></a><dl>
<dt><b>TBS_COMMAND_PRIORITY_HIGH</b></dt>
<dt>300 (0x12C)</dt>
</dl>
</td>
<td width="60%">
Used for high priority application use.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_COMMAND_PRIORITY_MAX"></a><a id="tbs_command_priority_max"></a><dl>
<dt><b>TBS_COMMAND_PRIORITY_MAX</b></dt>
<dt>2147483648 (0x80000000)</dt>
</dl>
</td>
<td width="60%">
Used for tasks that originate from the power management system.

</td>
</tr>
</table>

### -param pabCommand [in]

A pointer to a buffer that contains the TPM command to process.

### -param cbCommand [in]

The length, in bytes, of the command.

### -param pabResult [out]

A pointer to a buffer to receive the result of the TPM command.  This buffer can be the same as <i>pabCommand</i>.

### -param pcbResult [in, out]

An integer that, on input, specifies the size, in bytes, of the result buffer.  This value is set when the submit command returns.  If the supplied buffer is too small, this parameter, on output, is set to the required size, in bytes, for the result.

## -returns

If the function succeeds, the function returns TBS_SUCCESS.

A command can be submitted successfully and still fail at the TPM. In this case, the failure code is returned as a standard TPM error in the result buffer.

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
<dt><b>TBS_E_BUFFER_TOO_LARGE</b></dt>
<dt>2150121486 (0x8028400E)</dt>
</dl>
</td>
<td width="60%">
The input or output buffer is too large.

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
<dt><b>TBS_E_INSUFFICIENT_BUFFER</b></dt>
<dt>2150121477 (0x80284005)</dt>
</dl>
</td>
<td width="60%">
The specified output buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_CONTEXT</b></dt>
<dt>2150121476 (0x80284004)</dt>
</dl>
</td>
<td width="60%">
The specified context handle does not refer to a valid context.

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
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_IOERROR</b></dt>
<dt>2150121478 (0x80284006)</dt>
</dl>
</td>
<td width="60%">
An error occurred while communicating with the TPM.

</td>
</tr>
</table>

