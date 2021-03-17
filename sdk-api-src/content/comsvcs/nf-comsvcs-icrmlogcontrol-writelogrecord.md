---
UID: NF:comsvcs.ICrmLogControl.WriteLogRecord
title: ICrmLogControl::WriteLogRecord (comsvcs.h)
description: The CRM Worker and CRM Compensator use this method to write unstructured log records to the log.
helpviewer_keywords: ["ICrmLogControl interface [COM+]","WriteLogRecord method","ICrmLogControl.WriteLogRecord","ICrmLogControl::WriteLogRecord","WriteLogRecord","WriteLogRecord method [COM+]","WriteLogRecord method [COM+]","ICrmLogControl interface","_dtc_ICrmLogControl_WriteLogRecord","comsvcs/ICrmLogControl::WriteLogRecord","cos.icrmlogcontrol_writelogrecord"]
old-location: cos\icrmlogcontrol_writelogrecord.htm
tech.root: cos
ms.assetid: b2cbd9dc-5451-4aae-b2ce-28b2b93fd465
ms.date: 12/05/2018
ms.keywords: ICrmLogControl interface [COM+],WriteLogRecord method, ICrmLogControl.WriteLogRecord, ICrmLogControl::WriteLogRecord, WriteLogRecord, WriteLogRecord method [COM+], WriteLogRecord method [COM+],ICrmLogControl interface, _dtc_ICrmLogControl_WriteLogRecord, comsvcs/ICrmLogControl::WriteLogRecord, cos.icrmlogcontrol_writelogrecord
req.header: comsvcs.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICrmLogControl::WriteLogRecord
 - comsvcs/ICrmLogControl::WriteLogRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmLogControl.WriteLogRecord
---

# ICrmLogControl::WriteLogRecord


## -description

The CRM Worker and CRM Compensator use this method to write unstructured log records to the log. This method would typically be used by CRM components written in C++. Records are written lazily to the log and must be forced before they become durable. (See <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-forcelog">ICrmLogControl::ForceLog</a>.)

## -parameters

### -param rgBlob [in]

An array of BLOBs that form the log record. A BLOB is a Windows data type that is used to store an arbitrary amount of binary data.

### -param cBlob [in]

The number of BLOBs in the array.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The count of the number of BLOBs is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_WRONGSTATE</b></dt>
</dl>
</td>
<td width="60%">
This method was called in the wrong state; either before <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-registercompensator">RegisterCompensator</a> or when the transaction is completing (CRM Worker).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The transaction has aborted, most likely because of a transaction time-out.

</td>
</tr>
</table>

## -remarks

Unstructured records are simply a buffer of bytes. The method implements a gather capability by allowing sections of the specific CRM log record to be built up from an array of BLOBs, which is a structure containing a pointer to the data plus a count of the number of bytes. This reduces the copying of data, leading to only one copy directly from the CRM memory space into the buffer of the log manager.

Unstructured and structured log records cannot be mixed; either <b>WriteLogRecord</b> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants">WriteLogRecordVariants</a> can be called, but not both by the same CRM Worker or CRM Compensator.

You should not include pointer types within datastructures contained in BLOBs in a log record. Object references are no longer valid during recovery phase because the CRM Compensator runs in a different process than that of the CRM Worker that wrote the log record. Including pointer types within BLOBs in a log record can cause an application to crash or corrupt itself during recovery.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a>