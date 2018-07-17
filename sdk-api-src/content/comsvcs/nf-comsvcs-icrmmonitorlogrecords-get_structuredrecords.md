---
UID: NF:comsvcs.ICrmMonitorLogRecords.get_StructuredRecords
title: ICrmMonitorLogRecords::get_StructuredRecords
author: windows-sdk-content
description: Retrieves a flag indicating whether the log records written by this CRM clerk were structured.
old-location: cos\icrmmonitorlogrecords_get_structuredrecords.htm
old-project: cossdk
ms.assetid: a9b687c9-1e78-4896-a407-b069328ce66d
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICrmMonitorLogRecords interface [COM+],get_StructuredRecords method, ICrmMonitorLogRecords.get_StructuredRecords, ICrmMonitorLogRecords::get_StructuredRecords, _dtc_ICrmMonitorLogRecords_StructuredRecords, comsvcs/ICrmMonitorLogRecords::get_StructuredRecords, cos.icrmmonitorlogrecords_get_structuredrecords, get_StructuredRecords, get_StructuredRecords method [COM+], get_StructuredRecords method [COM+],ICrmMonitorLogRecords interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitorLogRecords.get_StructuredRecords
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmMonitorLogRecords::get_StructuredRecords


## -description


Retrieves a flag indicating whether the log records written by this CRM clerk were structured.


## -parameters




### -param pVal [out]

Indicates whether the log records are structured.
If this method is called before any log records have been written, this parameter is <b>TRUE</b>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5077ad2a-89c1-43f7-a7e0-7bd8036147b6">ICrmMonitorLogRecords</a>
 

 

