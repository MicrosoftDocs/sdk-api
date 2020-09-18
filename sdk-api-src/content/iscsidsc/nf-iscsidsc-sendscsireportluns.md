---
UID: NF:iscsidsc.SendScsiReportLuns
title: SendScsiReportLuns function (iscsidsc.h)
description: SendScsiReportLuns function sends a SCSI REPORT LUNS command to a specified target.
helpviewer_keywords: ["SendScsiReportLuns","SendScsiReportLuns function [iSCSI Discovery Library API]","iscsidisc.sendscsireportluns","iscsidsc/SendScsiReportLuns"]
old-location: iscsidisc\sendscsireportluns.htm
tech.root: iSCSIDisc
ms.assetid: 0898daf0-67ae-47a4-90bf-2112b6e6b20c
ms.date: 12/05/2018
ms.keywords: SendScsiReportLuns, SendScsiReportLuns function [iSCSI Discovery Library API], iscsidisc.sendscsireportluns, iscsidsc/SendScsiReportLuns
req.header: iscsidsc.h
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
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SendScsiReportLuns
 - iscsidsc/SendScsiReportLuns
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - SendScsiReportLuns
---

# SendScsiReportLuns function


## -description

<b>SendScsiReportLuns</b> function sends a SCSI REPORT LUNS command to a specified target.

## -parameters

### -param UniqueSessionId [in]

A pointer to a <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> structure that contains the session identifier for the login session of the target to query with the SCSI REPORT LUNS command.

### -param ScsiStatus [out]

A pointer to the location that receives the execution status of the CDB.

### -param ResponseSize [in, out]

A pointer to the location that, on input, specifies the byte-size of  <i>ResponseBuffer</i>. On output, this location specifies the number of bytes required to contain the response data for the READ CAPACITY command in the <i>ResponseBuffer</i>.

### -param ResponseBuffer [out]

The buffer that receives  response data for the READ CAPACITY command.

### -param SenseSize [in, out]

A pointer to a location that, on input, contains the byte-size of <i>SenseBuffer</i>. On output, the location pointed to receives the byte-size required for  <i>SenseBuffer</i>  to contain the sense data. This value will always be greater than or equal to 18 bytes.

### -param SenseBuffer [out]

The buffer that receives the sense data.

## -returns

Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer specified by <i>ResponseBuffer</i> is insufficient to hold the sense data.



If the device returns a SCSI error while processing the REPORT LUNS request, <b>SendScsiReportLuns</b> returns an error code of ISDSC_SCSI_REQUEST_FAILED, and the locations pointed to by <i>ScsiStatus</i> and <i>SenseBuffer</i> contain information detailing the SCSI error.

 

Otherwise, this function returns the appropriate Win32 or iSCSI error code on failure.

## -see-also

<a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>