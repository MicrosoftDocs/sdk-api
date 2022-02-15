---
UID: NE:faxcomex.FAX_JOB_EXTENDED_STATUS_ENUM
title: FAX_JOB_EXTENDED_STATUS_ENUM (faxcomex.h)
description: The FAX_JOB_EXTENDED_STATUS_ENUM enumeration defines the extended status values for a fax job.
helpviewer_keywords: ["FAX_JOB_EXTENDED_STATUS_ENUM","FAX_JOB_EXTENDED_STATUS_ENUM enumeration [Fax Service]","_mfax_fax_job_extended_status_enum","fax._mfax_fax_job_extended_status_enum","faxcomex/FAX_JOB_EXTENDED_STATUS_ENUM","faxcomex/fjesANSWERED","faxcomex/fjesBAD_ADDRESS","faxcomex/fjesBUSY","faxcomex/fjesCALL_ABORTED","faxcomex/fjesCALL_BLACKLISTED","faxcomex/fjesCALL_COMPLETED","faxcomex/fjesCALL_DELAYED","faxcomex/fjesDIALING","faxcomex/fjesDISCONNECTED","faxcomex/fjesFATAL_ERROR","faxcomex/fjesHANDLED","faxcomex/fjesINITIALIZING","faxcomex/fjesLINE_UNAVAILABLE","faxcomex/fjesNONE","faxcomex/fjesNOT_FAX_CALL","faxcomex/fjesNO_ANSWER","faxcomex/fjesNO_DIAL_TONE","faxcomex/fjesPARTIALLY_RECEIVED","faxcomex/fjesPROPRIETARY","faxcomex/fjesRECEIVING","faxcomex/fjesTRANSMITTING","fjesANSWERED","fjesBAD_ADDRESS","fjesBUSY","fjesCALL_ABORTED","fjesCALL_BLACKLISTED","fjesCALL_COMPLETED","fjesCALL_DELAYED","fjesDIALING","fjesDISCONNECTED","fjesFATAL_ERROR","fjesHANDLED","fjesINITIALIZING","fjesLINE_UNAVAILABLE","fjesNONE","fjesNOT_FAX_CALL","fjesNO_ANSWER","fjesNO_DIAL_TONE","fjesPARTIALLY_RECEIVED","fjesPROPRIETARY","fjesRECEIVING","fjesTRANSMITTING"]
old-location: fax\_mfax_fax_job_extended_status_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3w6l.htm
ms.date: 12/05/2018
ms.keywords: FAX_JOB_EXTENDED_STATUS_ENUM, FAX_JOB_EXTENDED_STATUS_ENUM enumeration [Fax Service], _mfax_fax_job_extended_status_enum, fax._mfax_fax_job_extended_status_enum, faxcomex/FAX_JOB_EXTENDED_STATUS_ENUM, faxcomex/fjesANSWERED, faxcomex/fjesBAD_ADDRESS, faxcomex/fjesBUSY, faxcomex/fjesCALL_ABORTED, faxcomex/fjesCALL_BLACKLISTED, faxcomex/fjesCALL_COMPLETED, faxcomex/fjesCALL_DELAYED, faxcomex/fjesDIALING, faxcomex/fjesDISCONNECTED, faxcomex/fjesFATAL_ERROR, faxcomex/fjesHANDLED, faxcomex/fjesINITIALIZING, faxcomex/fjesLINE_UNAVAILABLE, faxcomex/fjesNONE, faxcomex/fjesNOT_FAX_CALL, faxcomex/fjesNO_ANSWER, faxcomex/fjesNO_DIAL_TONE, faxcomex/fjesPARTIALLY_RECEIVED, faxcomex/fjesPROPRIETARY, faxcomex/fjesRECEIVING, faxcomex/fjesTRANSMITTING, fjesANSWERED, fjesBAD_ADDRESS, fjesBUSY, fjesCALL_ABORTED, fjesCALL_BLACKLISTED, fjesCALL_COMPLETED, fjesCALL_DELAYED, fjesDIALING, fjesDISCONNECTED, fjesFATAL_ERROR, fjesHANDLED, fjesINITIALIZING, fjesLINE_UNAVAILABLE, fjesNONE, fjesNOT_FAX_CALL, fjesNO_ANSWER, fjesNO_DIAL_TONE, fjesPARTIALLY_RECEIVED, fjesPROPRIETARY, fjesRECEIVING, fjesTRANSMITTING
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FAX_JOB_EXTENDED_STATUS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_JOB_EXTENDED_STATUS_ENUM
 - faxcomex/FAX_JOB_EXTENDED_STATUS_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_JOB_EXTENDED_STATUS_ENUM
---

# FAX_JOB_EXTENDED_STATUS_ENUM enumeration


## -description

The <b>FAX_JOB_EXTENDED_STATUS_ENUM</b> enumeration defines the extended status values for a fax job. These are basic values provided for developers of a fax service provider (FSP). However, with the exception of <b><b>fjesPARTIALLY_RECEIVED</b></b>, these values or other proprietary values that may be developed for a specific FSP, are not recognized or interpreted by the fax server.

## -enum-fields

### -field fjesNONE:0

No extended status value.

### -field fjesDISCONNECTED

The sender or the caller disconnected the fax call.

### -field fjesINITIALIZING

The device is initializing a call.

### -field fjesDIALING

The device is dialing a fax number.

### -field fjesTRANSMITTING

The device is sending a fax.

### -field fjesANSWERED

The device answered a new call.

### -field fjesRECEIVING

The device is receiving a fax.

### -field fjesLINE_UNAVAILABLE

The device is not available because it is in use by another application.

### -field fjesBUSY

The device encountered a busy signal.

### -field fjesNO_ANSWER

The receiving device did not answer the call.

### -field fjesBAD_ADDRESS

The device dialed an invalid fax number.

### -field fjesNO_DIAL_TONE

The sending device cannot complete the call because it does not detect a dial tone.

### -field fjesFATAL_ERROR

The device has encountered a fatal protocol error.

### -field fjesCALL_DELAYED

The device delayed a fax call because the sending device received a busy signal multiple times. The device cannot retry the call because dialing restrictions exist. (Some countries/regions restrict the number of retry attempts when a number is busy.)

### -field fjesCALL_BLACKLISTED

The device could not complete a call because the telephone number was blocked or reserved; emergency numbers such as 911 are blocked.

### -field fjesNOT_FAX_CALL

The device received a call that was a data call or a voice call.

### -field fjesPARTIALLY_RECEIVED

The incoming fax was partially received. Some (but not all) of the pages are available.

### -field fjesHANDLED

The fax service processed the outbound fax; the fax service provider will transmit the fax.

### -field fjesCALL_COMPLETED

The call was completed.

### -field fjesCALL_ABORTED

The call was aborted.

### -field fjesPROPRIETARY:0x1000000

Obsolete. For information about proprietary extended status codes, see <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatuscode-vb">IFaxOutgoingJob::get_ExtendedStatusCode</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-extendedstatuscode">ExtendedStatusCode</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-extendedstatus-vb">IFaxIncomingJob::get_ExtendedStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus-extendedstatus-vb">IFaxJobStatus::get_ExtendedStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus-extendedstatuscode-vb">IFaxJobStatus::get_ExtendedStatusCode</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatus-vb">IFaxOutgoingJob::get_ExtendedStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatuscode-vb">IFaxOutgoingJob::get_ExtendedStatusCode</a>
