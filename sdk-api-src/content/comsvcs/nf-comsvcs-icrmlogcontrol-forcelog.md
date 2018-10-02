---
UID: NF:comsvcs.ICrmLogControl.ForceLog
title: ICrmLogControl::ForceLog
author: windows-sdk-content
description: Forces all log records to be durable on disk.
old-location: cos\icrmlogcontrol_forcelog.htm
tech.root: cossdk
ms.assetid: 547c9e31-62a0-413e-8371-20356bfe8906
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ForceLog, ForceLog method [COM+], ForceLog method [COM+],ICrmLogControl interface, ICrmLogControl interface [COM+],ForceLog method, ICrmLogControl.ForceLog, ICrmLogControl::ForceLog, _dtc_ICrmLogControl_ForceLog, comsvcs/ICrmLogControl::ForceLog, cos.icrmlogcontrol_forcelog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmLogControl.ForceLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmLogControl::ForceLog


## -description


Forces all log records to be durable on disk.


## -parameters






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



The CRM Worker and CRM Compensator use this method to write log records lazily to the log, which means they are not made durable until they have been forced to the log. Calling <b>ForceLog</b> will make all log records that have been written durable on disk.




## -see-also




<a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a>
 

 

