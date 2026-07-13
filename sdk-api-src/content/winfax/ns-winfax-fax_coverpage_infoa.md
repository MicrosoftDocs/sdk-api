---
UID: NS:winfax._FAX_COVERPAGE_INFOA
title: FAX_COVERPAGE_INFOA (winfax.h)
description: The FAX_COVERPAGE_INFO structure contains data to display on the cover page of a fax transmission. The SizeOfStruct and CoverPageName members are required; other members are optional. (ANSI)
helpviewer_keywords: ["*PFAX_COVERPAGE_INFOA","FAX_COVERPAGE_INFO","FAX_COVERPAGE_INFO structure [Fax Service]","FAX_COVERPAGE_INFOA","FAX_COVERPAGE_INFOW","PFAX_COVERPAGE_INFO","PFAX_COVERPAGE_INFO structure pointer [Fax Service]","_mfax_fax_coverpage_info_str","fax._mfax_fax_coverpage_info_str","winfax/FAX_COVERPAGE_INFO","winfax/FAX_COVERPAGE_INFOA","winfax/FAX_COVERPAGE_INFOW","winfax/PFAX_COVERPAGE_INFO"]
old-location: fax\_mfax_fax_coverpage_info_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3zaq.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_COVERPAGE_INFOA, FAX_COVERPAGE_INFO, FAX_COVERPAGE_INFO structure [Fax Service], FAX_COVERPAGE_INFOA, FAX_COVERPAGE_INFOW, PFAX_COVERPAGE_INFO, PFAX_COVERPAGE_INFO structure pointer [Fax Service], _mfax_fax_coverpage_info_str, fax._mfax_fax_coverpage_info_str, winfax/FAX_COVERPAGE_INFO, winfax/FAX_COVERPAGE_INFOA, winfax/FAX_COVERPAGE_INFOW, winfax/PFAX_COVERPAGE_INFO'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_COVERPAGE_INFOW (Unicode) and FAX_COVERPAGE_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_COVERPAGE_INFOA, *PFAX_COVERPAGE_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_COVERPAGE_INFOA
 - winfax/_FAX_COVERPAGE_INFOA
 - PFAX_COVERPAGE_INFOA
 - winfax/PFAX_COVERPAGE_INFOA
 - FAX_COVERPAGE_INFOA
 - winfax/FAX_COVERPAGE_INFOA
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
 - FAX_COVERPAGE_INFO
 - FAX_COVERPAGE_INFOA
 - FAX_COVERPAGE_INFOW
---

# FAX_COVERPAGE_INFOA structure


## -description

The <b>FAX_COVERPAGE_INFO</b> structure contains data to display on the cover page of a fax transmission. The <b>SizeOfStruct</b> and <b>CoverPageName</b> members are required; other members are optional.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_COVERPAGE_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_COVERPAGE_INFO)</b>.

### -field CoverPageName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the name of the cover page file (.cov) to associate with the received fax document. The string can be the file name of the common cover page file, or it can be the UNC path to a local cover page file.

### -field UseServerCoverPage

Type: <b>BOOL</b>

Specifies a Boolean variable that indicates whether the fax cover page file is stored on the local computer or in the common cover page location. A value of <b>TRUE</b> indicates that the cover page file resides in the common cover page location on the fax server.

### -field RecName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the recipient of the fax transmission.

### -field RecFaxNumber

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the fax number of the recipient of the fax transmission.

### -field RecCompany

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the company name of the recipient of the fax transmission.

### -field RecStreetAddress

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the street address of the recipient of the fax transmission.

### -field RecCity

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the city of the recipient of the fax transmission.

### -field RecState

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the state of the recipient of the fax transmission.

### -field RecZip

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the postal ZIP code of the recipient of the fax transmission.

### -field RecCountry

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the country/region of the recipient of the fax transmission.

### -field RecTitle

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the title of the recipient of the fax transmission.

### -field RecDepartment

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the department of the recipient of the fax transmission.

### -field RecOfficeLocation

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office location of the recipient of the fax transmission.

### -field RecHomePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the home telephone number of the recipient of the fax transmission.

### -field RecOfficePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office telephone number of the recipient of the fax transmission.

### -field SdrName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the name of the sender who initiated the fax transmission.

### -field SdrFaxNumber

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the fax number of the sender who initiated the fax transmission.

### -field SdrCompany

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the company name of the sender who initiated the fax transmission.

### -field SdrAddress

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the address of the sender who initiated the fax transmission.

### -field SdrTitle

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the title of the sender who initiated the fax transmission.

### -field SdrDepartment

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the department name of the sender who initiated the fax transmission.

### -field SdrOfficeLocation

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office location of the sender who initiated the fax transmission.

### -field SdrHomePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the home telephone number of the sender who initiated the fax transmission.

### -field SdrOfficePhone

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the office telephone number of the sender who initiated the fax transmission.

### -field Note

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the text of a message or note from the sender that pertains to the fax transmission. The text will appear on the cover page.

### -field Subject

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the subject line of the fax transmission.

### -field TimeSent

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

Specifies a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. The fax server sets this member when it initiates the fax transmission. The time is expressed in local system time.

### -field PageCount

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the total number of pages in the fax transmission.

## -remarks

A fax client application passes the <b>FAX_COVERPAGE_INFO</b> structure in a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a> function. This enables a user to print a personal cover page at the beginning of a fax transmission. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-cover-pages">Cover Pages</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.





> [!NOTE]
> The winfax.h header defines FAX_COVERPAGE_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxcompletejobparamsa">FaxCompleteJobParams</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>
