---
UID: NF:comsvcs.ICrmMonitorLogRecords.get_Count
title: ICrmMonitorLogRecords::get_Count (comsvcs.h)
description: Retrieves the number of log records written by this CRM clerk.
helpviewer_keywords: ["ICrmMonitorLogRecords interface [COM+]","get_Count method","ICrmMonitorLogRecords.get_Count","ICrmMonitorLogRecords::get_Count","_dtc_ICrmMonitorLogRecords_Count","comsvcs/ICrmMonitorLogRecords::get_Count","cos.icrmmonitorlogrecords_get_count","get_Count","get_Count method [COM+]","get_Count method [COM+]","ICrmMonitorLogRecords interface"]
old-location: cos\icrmmonitorlogrecords_get_count.htm
tech.root: cos
ms.assetid: 51acc910-a38a-4747-bf99-b468f7ffddd1
ms.date: 12/05/2018
ms.keywords: ICrmMonitorLogRecords interface [COM+],get_Count method, ICrmMonitorLogRecords.get_Count, ICrmMonitorLogRecords::get_Count, _dtc_ICrmMonitorLogRecords_Count, comsvcs/ICrmMonitorLogRecords::get_Count, cos.icrmmonitorlogrecords_get_count, get_Count, get_Count method [COM+], get_Count method [COM+],ICrmMonitorLogRecords interface
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
 - ICrmMonitorLogRecords::get_Count
 - comsvcs/ICrmMonitorLogRecords::get_Count
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
 - ICrmMonitorLogRecords.get_Count
---

# ICrmMonitorLogRecords::get_Count


## -description

Retrieves the number of log records written by this CRM clerk.

## -parameters

### -param pVal [out]

The number of log records written by this CRM clerk.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorlogrecords">ICrmMonitorLogRecords</a>