---
UID: NF:winscard.GetOpenCardNameA
title: GetOpenCardNameA function (winscard.h)
description: The GetOpenCardName function displays the smart card &quot;select card&quot; dialog box. (ANSI)
helpviewer_keywords: ["GetOpenCardNameA", "winscard/GetOpenCardNameA"]
old-location: security\getopencardname.htm
tech.root: security
ms.assetid: b103cec0-dd28-4f90-864b-5f66d044ec55
ms.date: 12/05/2018
ms.keywords: GetOpenCardName, GetOpenCardName function [Security], GetOpenCardNameA, GetOpenCardNameW, _smart_getopencardname, security.getopencardname, winscard/GetOpenCardName, winscard/GetOpenCardNameA, winscard/GetOpenCardNameW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetOpenCardNameW (Unicode) and GetOpenCardNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Scarddlg.lib
req.dll: Scarddlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetOpenCardNameA
 - winscard/GetOpenCardNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Scarddlg.dll
api_name:
 - GetOpenCardName
 - GetOpenCardNameA
 - GetOpenCardNameW
---

# GetOpenCardNameA function


## -description

The <b>GetOpenCardName</b> function displays the <a href="/windows/desktop/SecGloss/s-gly">smart card</a> "select card" dialog box. Call the function 
<a href="/windows/desktop/api/winscard/nf-winscard-scarduidlgselectcarda">SCardUIDlgSelectCard</a> instead of <b>GetOpenCardName</b>. The <b>GetOpenCardName</b> function is maintained for backward compatibility with version 1.0 of the Microsoft Smart Card Base Components, but calls to <b>GetOpenCardName</b> are mapped to <b>SCardUIDlgSelectCard</b>.

## -parameters

### -param unnamedParam1 [in]

A pointer to the 
<a href="/windows/desktop/api/winscard/ns-winscard-opencardnamea">OPENCARDNAME</a> structure for the "select card" dialog box.

## -returns

The function returns different values depending on whether it succeeds or fails.
						
						
					

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winscard/ns-winscard-opencardnamea">OPENCARDNAME</a>

## -remarks

> [!NOTE]
> The winscard.h header defines GetOpenCardName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
