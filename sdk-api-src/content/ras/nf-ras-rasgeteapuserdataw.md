---
UID: NF:ras.RasGetEapUserDataW
title: RasGetEapUserDataW function (ras.h)
description: Use the RasGetEapUserData function to retrieve user-specific Extensible Authentication Protocol (EAP) information for the specified phone-book entry. (Unicode)
helpviewer_keywords: ["RasGetEapUserData", "RasGetEapUserData function [RAS]", "RasGetEapUserDataW", "_ras_rasgeteapuserdata", "ras/RasGetEapUserData", "ras/RasGetEapUserDataW", "rras.rasgeteapuserdata"]
old-location: rras\rasgeteapuserdata.htm
tech.root: RRAS
ms.assetid: 6b1a1c73-28af-43ff-b79c-c796ddae219c
ms.date: 12/05/2018
ms.keywords: RasGetEapUserData, RasGetEapUserData function [RAS], RasGetEapUserDataA, RasGetEapUserDataW, _ras_rasgeteapuserdata, ras/RasGetEapUserData, ras/RasGetEapUserDataA, ras/RasGetEapUserDataW, rras.rasgeteapuserdata
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetEapUserDataW (Unicode) and RasGetEapUserDataA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasGetEapUserDataW
 - ras/RasGetEapUserDataW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasGetEapUserData
 - RasGetEapUserDataA
 - RasGetEapUserDataW
---

# RasGetEapUserDataW function


## -description

Use the 
<b>RasGetEapUserData</b> function to retrieve user-specific Extensible Authentication Protocol (EAP) information for the specified phone-book entry.

## -parameters

### -param hToken [in]

Handle to a primary or impersonation access token that represents the user for which to retrieve data. This parameter can be <b>NULL</b> if the function is called from a process already running in the user's context.

### -param pszPhonebook [in]

Pointer to a null-terminated string that specifies the full path of the phone-book (PBK) file. If this parameter is <b>NULL</b>, the function  uses the system phone book.

### -param pszEntry [in]

Pointer to a null-terminated string that specifies an existing entry name.

### -param pbEapData [out]

Pointer to a buffer that receives the retrieved EAP data for the user. The caller should allocate the memory for this buffer. If the buffer is not large enough, 
<b>RasGetEapUserData</b>  returns <b>ERROR_BUFFER_TOO_SMALL</b>, and the <i>pdwSizeofEapData</i> parameter  contains the required size.

### -param pdwSizeofEapData [in, out]

Pointer to a <b>DWORD</b> variable that, on input, specifies the size of the buffer pointed to by the <i>pbEapData</i> parameter. 




If the buffer specified by the <i>pbEapData</i> parameter is not large enough, <i>pdwSizeofEapData</i> receives, on output, the required size.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSizeofEapData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>pbEapData</i> is too small to receive the data. The <i>pdwSizeofEapData</i> contains the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuserdataa">RasGetEapUserData</a> was unable to open the specified phone-book file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuserdataa">RasGetEapUserData</a> was unable to find the specified entry in the phone book.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377242(v=vs.85)">RASEAPINFO</a>



<a href="/windows/desktop/api/ras/nf-ras-rasseteapuserdataa">RasSetEapUserData</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>

## -remarks

> [!NOTE]
> The ras.h header defines RasGetEapUserData as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
