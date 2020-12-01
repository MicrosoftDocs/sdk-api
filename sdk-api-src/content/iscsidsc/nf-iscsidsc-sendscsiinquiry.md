---
UID: NF:iscsidsc.SendScsiInquiry
title: SendScsiInquiry function (iscsidsc.h)
description: SendScsiInquiry function sends a SCSI INQUIRY command to the specified target.
helpviewer_keywords: ["SendScsiInquiry","SendScsiInquiry function [iSCSI Discovery Library API]","iscsidisc.sendscsiinquiry","iscsidsc/SendScsiInquiry"]
old-location: iscsidisc\sendscsiinquiry.htm
tech.root: iSCSIDisc
ms.assetid: a1339ff0-aa1e-4609-8983-d5f09481bd13
ms.date: 12/05/2018
ms.keywords: SendScsiInquiry, SendScsiInquiry function [iSCSI Discovery Library API], iscsidisc.sendscsiinquiry, iscsidsc/SendScsiInquiry
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
 - SendScsiInquiry
 - iscsidsc/SendScsiInquiry
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
 - SendScsiInquiry
---

# SendScsiInquiry function


## -description

The <b>SendScsiInquiry</b> function sends a SCSI INQUIRY command to the specified target.

## -parameters

### -param UniqueSessionId [in]

A pointer to a <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> structure containing the session identifier for the login session specific to the target to which the READ CAPACITY command is sent.

### -param Lun [in]

The logical unit to query for SCSI inquiry data.

### -param EvpdCmddt [in]

The values to assign to the EVP (enable the vital product data) and CmdDt (command support data) bits in the INQUIRY command. Bits 0 (EVP) and 1 (CmdDt) of the <i>EvpdCmddt</i> parameter 
are inserted into bits 0 and 1, respectively, of the second byte of the Command Descriptor Block (CDB) of the <b>INQUIRY</b> command.

### -param PageCode [in]

The page code. This code is inserted into the third byte of the CDB of the <b>INQUIRY</b> command.

### -param ScsiStatus [out]

A pointer to a location that reports the execution status of the CDB.

### -param ResponseSize [in, out]

A pointer to the location that, on input, specifies the byte-size of  <i>ResponseBuffer</i>. On output, this location specifies the number of bytes required to contain the response data for the READ CAPACITY command in the <i>ResponseBuffer</i>.

### -param ResponseBuffer [out]

The buffer that holds the inquiry data.

### -param SenseSize [in, out]

A pointer to a location that, on input, contains the byte-size of <i>SenseBuffer</i>. On output, the location pointed to receives the byte-size required for  <i>SenseBuffer</i>  to contain the sense data. This value will always be greater than or equal to 18 bytes.

### -param SenseBuffer [out]

The buffer that holds the sense data.

## -returns

Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer specified by <i>ResponseBuffer</i> is insufficient to contain the sense data.



If the device returns a SCSI error while processing the REPORT LUNS request, <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsireportluns">SendScsiReportLuns</a> returns an error code of ISDSC_SCSI_REQUEST_FAILED, and the locations pointed to by <i>ScsiStatus</i> and <i>SenseBuffer</i> contain information detailing the SCSI error.

 

Otherwise, <b>SendScsiInquiry</b> returns the appropriate Win32 or iSCSI error code on failure.

## -see-also

<a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>