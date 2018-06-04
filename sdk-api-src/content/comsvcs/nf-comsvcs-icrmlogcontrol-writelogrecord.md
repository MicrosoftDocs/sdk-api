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

# ICrmLogControl::WriteLogRecord


## -description


The CRM Worker and CRM Compensator use this method to write unstructured log records to the log. This method would typically be used by CRM components written in C++. Records are written lazily to the log and must be forced before they become durable. (See <a href="https://msdn.microsoft.com/547c9e31-62a0-413e-8371-20356bfe8906">ICrmLogControl::ForceLog</a>.)



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
This method was called in the wrong state; either before <a href="https://msdn.microsoft.com/f7907dff-a4a1-4526-8dab-547e819199ec">RegisterCompensator</a> or when the transaction is completing (CRM Worker).

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

Unstructured and structured log records cannot be mixed; either <b>WriteLogRecord</b> or <a href="https://msdn.microsoft.com/ebd3943d-0c77-49fe-a53e-bc0c45e13a54">WriteLogRecordVariants</a> can be called, but not both by the same CRM Worker or CRM Compensator.

You should not include pointer types within datastructures contained in BLOBs in a log record. Object references are no longer valid during recovery phase because the CRM Compensator runs in a different process than that of the CRM Worker that wrote the log record. Including pointer types within BLOBs in a log record can cause an application to crash or corrupt itself during recovery.




## -see-also




<a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a>
 

 

