---
UID: NS:winfax._FAX_CONTEXT_INFOA
title: FAX_CONTEXT_INFOA (winfax.h)
description: The FAX_CONTEXT_INFO structure contains information about a fax printer device context. The SizeOfStruct member is required. Information for the other members is supplied by a call to the FaxStartPrintJob function. (ANSI)
helpviewer_keywords: ["*PFAX_CONTEXT_INFOA","FAX_CONTEXT_INFO","FAX_CONTEXT_INFO structure [Fax Service]","FAX_CONTEXT_INFOA","FAX_CONTEXT_INFOW","PFAX_CONTEXT_INFO","PFAX_CONTEXT_INFO structure pointer [Fax Service]","_mfax_fax_context_info_str","fax._mfax_fax_context_info_str","winfax/FAX_CONTEXT_INFO","winfax/FAX_CONTEXT_INFOA","winfax/FAX_CONTEXT_INFOW","winfax/PFAX_CONTEXT_INFO"]
old-location: fax\_mfax_fax_context_info_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7v5e.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_CONTEXT_INFOA, FAX_CONTEXT_INFO, FAX_CONTEXT_INFO structure [Fax Service], FAX_CONTEXT_INFOA, FAX_CONTEXT_INFOW, PFAX_CONTEXT_INFO, PFAX_CONTEXT_INFO structure pointer [Fax Service], _mfax_fax_context_info_str, fax._mfax_fax_context_info_str, winfax/FAX_CONTEXT_INFO, winfax/FAX_CONTEXT_INFOA, winfax/FAX_CONTEXT_INFOW, winfax/PFAX_CONTEXT_INFO'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_CONTEXT_INFOW (Unicode) and FAX_CONTEXT_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_CONTEXT_INFOA, *PFAX_CONTEXT_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_CONTEXT_INFOA
 - winfax/_FAX_CONTEXT_INFOA
 - PFAX_CONTEXT_INFOA
 - winfax/PFAX_CONTEXT_INFOA
 - FAX_CONTEXT_INFOA
 - winfax/FAX_CONTEXT_INFOA
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
 - FAX_CONTEXT_INFO
 - FAX_CONTEXT_INFOA
 - FAX_CONTEXT_INFOW
---

# FAX_CONTEXT_INFOA structure


## -description

The <b>FAX_CONTEXT_INFO</b> structure contains information about a fax printer device context. The <b>SizeOfStruct</b> member is required. Information for the other members is supplied by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_CONTEXT_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_CONTEXT_INFO)</b> before it calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function.

### -field hDC

Type: <b>HDC</b>

Handle to a fax printer device context. A call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function supplies the data for this member.

### -field ServerName

Type: <b>TCHAR[MAX_COMPUTERNAME_LENGTH+1]</b>

Specifies a variable that contains a null-terminated string that is the fax server name of interest. A call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function supplies the data for this member. If the fax server is on the local computer, this member will be empty. The client application does not need to fill in this member.

## -remarks

A fax client application can call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function to retrieve the handle to a fax printer device context. The function returns the handle in a <b>FAX_CONTEXT_INFO</b> structure. The application must call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function to deallocate the handle to the printer device context. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-printing-a-fax-to-a-device-context">Printing a Fax to a Device Context</a>.





> [!NOTE]
> The winfax.h header defines FAX_CONTEXT_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a>
