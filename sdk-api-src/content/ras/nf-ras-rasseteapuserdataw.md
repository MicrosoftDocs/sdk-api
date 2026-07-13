---
UID: NF:ras.RasSetEapUserDataW
title: RasSetEapUserDataW function (ras.h)
description: Use the RasSetEapUserData function to store user-specific Extensible Authentication Protocol (EAP) information for the specified phone-book entry in the registry. (Unicode)
helpviewer_keywords: ["RasSetEapUserData", "RasSetEapUserData function [RAS]", "RasSetEapUserDataW", "_ras_rasseteapuserdata", "ras/RasSetEapUserData", "ras/RasSetEapUserDataW", "rras.rasseteapuserdata"]
old-location: rras\rasseteapuserdata.htm
tech.root: RRAS
ms.assetid: 702e5c42-cc8c-43cf-a0bf-d3e450c031a4
ms.date: 12/05/2018
ms.keywords: RasSetEapUserData, RasSetEapUserData function [RAS], RasSetEapUserDataA, RasSetEapUserDataW, _ras_rasseteapuserdata, ras/RasSetEapUserData, ras/RasSetEapUserDataA, ras/RasSetEapUserDataW, rras.rasseteapuserdata
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetEapUserDataW (Unicode) and RasSetEapUserDataA (ANSI)
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
 - RasSetEapUserDataW
 - ras/RasSetEapUserDataW
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
 - RasSetEapUserData
 - RasSetEapUserDataA
 - RasSetEapUserDataW
---

# RasSetEapUserDataW function


## -description

Use the 
<b>RasSetEapUserData</b> function to store user-specific Extensible Authentication Protocol (EAP) information for the specified phone-book entry in the registry.

## -parameters

### -param hToken [in]

Handle to a primary or impersonation access token that represents the user for which to store data. This parameter can be <b>NULL</b> if the function is called from a process already running in the user's context.

### -param pszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the phone-book (PBK) file. If this parameter is <b>NULL</b>, the function  uses the system phone book.

### -param pszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies an existing entry name.

### -param pbEapData [in]

Pointer to the data to store for the user.

### -param dwSizeofEapData [in]

Specifies the size of the data pointed to by the <i>pbEapData</i> parameter.

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
The <i>dwSizeofEapData</i> parameter is zero, or the <i>pbEapData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
<b>RasSetEapUserData</b> was unable to open the specified phone-book file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
<b>RasSetEapUserData</b> was unable to find the specified entry in the phone book.

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

<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuserdataa">RasGetEapUserData</a>



<a href="/windows/desktop/api/ras/nf-ras-rasinvokeeapui">RasInvokeEapUI</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>

## -remarks

> [!NOTE]
> The ras.h header defines RasSetEapUserData as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
