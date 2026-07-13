---
UID: NS:winfax._FAX_PRINT_INFOA
title: FAX_PRINT_INFOA (winfax.h)
description: The FAX_PRINT_INFO structure contains the information necessary for the fax server to print a fax transmission. The structure includes sender and recipient data, an optional billing code, and delivery report information. (ANSI)
helpviewer_keywords: ["*PFAX_PRINT_INFOA","FAX_PRINT_INFO","FAX_PRINT_INFO structure [Fax Service]","FAX_PRINT_INFOA","FAX_PRINT_INFOW","PFAX_PRINT_INFO","PFAX_PRINT_INFO structure pointer [Fax Service]","_mfax_fax_print_info_str","fax._mfax_fax_print_info_str","winfax/FAX_PRINT_INFO","winfax/FAX_PRINT_INFOA","winfax/FAX_PRINT_INFOW","winfax/PFAX_PRINT_INFO"]
old-location: fax\_mfax_fax_print_info_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_60he.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_PRINT_INFOA, FAX_PRINT_INFO, FAX_PRINT_INFO structure [Fax Service], FAX_PRINT_INFOA, FAX_PRINT_INFOW, PFAX_PRINT_INFO, PFAX_PRINT_INFO structure pointer [Fax Service], _mfax_fax_print_info_str, fax._mfax_fax_print_info_str, winfax/FAX_PRINT_INFO, winfax/FAX_PRINT_INFOA, winfax/FAX_PRINT_INFOW, winfax/PFAX_PRINT_INFO'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_PRINT_INFOW (Unicode) and FAX_PRINT_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_PRINT_INFOA, *PFAX_PRINT_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_PRINT_INFOA
 - winfax/_FAX_PRINT_INFOA
 - PFAX_PRINT_INFOA
 - winfax/PFAX_PRINT_INFOA
 - FAX_PRINT_INFOA
 - winfax/FAX_PRINT_INFOA
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
 - FAX_PRINT_INFO
 - FAX_PRINT_INFOA
 - FAX_PRINT_INFOW
---

# FAX_PRINT_INFOA structure


## -description

The <b>FAX_PRINT_INFO</b> structure contains the information necessary for the fax server to print a fax transmission. The structure includes sender and recipient data, an optional billing code, and delivery report information.

The <b>SizeOfStruct</b> and <b>RecipientNumber</b> members are required; other members are optional.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_PRINT_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_PRINT_INFO)</b>. This member is required.

### -field DocName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the user-friendly name that appears in the print spooler.

### -field RecipientName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the recipient of the fax transmission.

### -field RecipientNumber

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the fax number of the recipient of the fax transmission. This member is required.

### -field SenderName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the sender who initiated the fax transmission.

### -field SenderCompany

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the company name of the sender who initiated the fax transmission.

### -field SenderDept

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the department name of the sender who initiated the fax transmission.

### -field SenderBillingCode

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that indicates an application- or server-specific billing code that applies to the fax transmission. The fax server uses the string to generate an entry in the fax event log. Billing codes are optional.

### -field Reserved

Type: <b>LPCTSTR</b>

Reserved. Must be set to <b>NULL</b>.

### -field DrEmailAddress

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the email address to which the fax server should send the delivery report (DR) or nondelivery report (NDR).

### -field OutputFileName

Type: <b>LPCTSTR</b>

This member is reserved for future use by Microsoft. It must be set to <b>NULL</b>.

## -remarks

A fax client application passes the <b>FAX_PRINT_INFO</b> structure in a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function to start a print job on a specified fax printer. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-printing-a-fax-to-a-device-context">Printing a Fax to a Device Context</a>.





> [!NOTE]
> The winfax.h header defines FAX_PRINT_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a>
