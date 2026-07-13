---
UID: NS:winfax._FAX_JOB_PARAMA
title: FAX_JOB_PARAMA (winfax.h)
description: The FAX_JOB_PARAM structure contains the information necessary for the fax server to send an individual fax transmission. (ANSI)
helpviewer_keywords: ["*PFAX_JOB_PARAMA","DRT_EMAIL","DRT_INBOX","DRT_NONE","FAX_JOB_PARAM","FAX_JOB_PARAM structure [Fax Service]","FAX_JOB_PARAMA","FAX_JOB_PARAMW","JSA_DISCOUNT_PERIOD","JSA_NOW","JSA_SPECIFIC_TIME","PFAX_JOB_PARAM","PFAX_JOB_PARAM structure pointer [Fax Service]","_mfax_fax_job_param_str","fax._mfax_fax_job_param_str","winfax/FAX_JOB_PARAM","winfax/FAX_JOB_PARAMA","winfax/FAX_JOB_PARAMW","winfax/PFAX_JOB_PARAM"]
old-location: fax\_mfax_fax_job_param_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_21yq.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_JOB_PARAMA, DRT_EMAIL, DRT_INBOX, DRT_NONE, FAX_JOB_PARAM, FAX_JOB_PARAM structure [Fax Service], FAX_JOB_PARAMA, FAX_JOB_PARAMW, JSA_DISCOUNT_PERIOD, JSA_NOW, JSA_SPECIFIC_TIME, PFAX_JOB_PARAM, PFAX_JOB_PARAM structure pointer [Fax Service], _mfax_fax_job_param_str, fax._mfax_fax_job_param_str, winfax/FAX_JOB_PARAM, winfax/FAX_JOB_PARAMA, winfax/FAX_JOB_PARAMW, winfax/PFAX_JOB_PARAM'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_JOB_PARAMW (Unicode) and FAX_JOB_PARAMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_JOB_PARAMA, *PFAX_JOB_PARAMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_JOB_PARAMA
 - winfax/_FAX_JOB_PARAMA
 - PFAX_JOB_PARAMA
 - winfax/PFAX_JOB_PARAMA
 - FAX_JOB_PARAMA
 - winfax/FAX_JOB_PARAMA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winfax.h
api_name:
 - FAX_JOB_PARAM
 - FAX_JOB_PARAMA
 - FAX_JOB_PARAMW
---

# FAX_JOB_PARAMA structure


## -description

The <b>FAX_JOB_PARAM</b> structure contains the information necessary for the fax server to send an individual fax transmission. The structure includes the recipient's fax number, sender and recipient data, an optional billing code, and job scheduling information.

The <b>SizeOfStruct</b>, <b>RecipientNumber</b>, and <b>ScheduleAction</b> members are required; other members are optional.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_JOB_PARAM</b> structure. The calling application must set this member to <b>sizeof(FAX_JOB_PARAM)</b>. This member is required.

### -field RecipientNumber

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the fax number of the recipient of the fax transmission. This member is required.

### -field RecipientName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the recipient of the fax transmission.

### -field Tsid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the transmitting station identifier (TSID). This identifier is usually a telephone number. Only printable characters such as English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) can be used in a TSID.

### -field SenderName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the sender who initiated the fax transmission.

### -field SenderCompany

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the company name of the sender who initiated the fax transmission.

### -field SenderDept

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the department name of the sender who initiated the fax transmission.

### -field BillingCode

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that indicates an application- or server-specific billing code that applies to the fax transmission. The fax server uses the string to generate an entry in the fax event log. Billing codes are optional.

### -field ScheduleAction

Type: <b>DWORD</b>

Specifies a DWORD variable that indicates when to send the fax. This member is required, and can be one of the following predefined job scheduling actions. 



#### JSA_NOW

Send the fax as soon as a device is available. 



#### JSA_SPECIFIC_TIME

Send the fax at the time specified by the <b>ScheduleTime</b> member. 



#### JSA_DISCOUNT_PERIOD

Send the fax during the discount rate period. Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetconfigurationa">FaxGetConfiguration</a> function to retrieve the discount period for the fax server.

### -field ScheduleTime

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

If the <b>ScheduleAction</b> member is equal to the value <b>JSA_SPECIFIC_TIME</b>, specifies a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date and time to send the fax. The time specified must be expressed in UTC.

### -field DeliveryReportType

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the type of email delivery report (DR) or nondelivery report (NDR) that the fax server should generate. This member can be one of the following predefined delivery report types. 



#### DRT_NONE

Do not send a DR or an NDR to the sender of the fax transmission. 



#### DRT_EMAIL

Send the DR or NDR in an email message to the sender of the fax transmission (supported in Windows Server 2003 and later). 



#### DRT_INBOX

Send the DR or NDR in email to the sender's local personal information store.

### -field DeliveryReportAddress

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string. If the <b>DeliveryReportType</b> member is equal to <b>DRT_EMAIL</b>, the string is the address to which the DR or NDR should be sent. If the <b>DeliveryReportType</b> member is equal to <b>DRT_NONE</b>, this member must be <b>NULL</b>.

### -field DocumentName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string to associate with the fax document. This is the user-friendly name that appears in the print spooler.

### -field CallHandle

Type: <b>HCALL</b>

Reserved, and should be <b>NULL</b>.

### -field Reserved

Type: <b>DWORD_PTR[3]</b>

This member is reserved for future use by Microsoft. It must be set to zero.

## -remarks

A fax client application passes the <b>FAX_JOB_PARAM</b> structure in a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a> function to inform the fax server how and when to send the fax transmission. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax-to-one-recipient-win32-environment-">Sending a Fax to One Recipient (Win32 Environment)</a>.





> [!NOTE]
> The winfax.h header defines FAX_JOB_PARAM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxcompletejobparamsa">FaxCompleteJobParams</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetconfigurationa">FaxGetConfiguration</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>
