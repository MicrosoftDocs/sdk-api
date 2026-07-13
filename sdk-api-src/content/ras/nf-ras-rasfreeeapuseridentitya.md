---
UID: NF:ras.RasFreeEapUserIdentityA
title: RasFreeEapUserIdentityA function (ras.h)
description: Use the RasFreeEapUserIdentity function to free the memory buffer returned by RasGetEapUserIdentity. (ANSI)
helpviewer_keywords: ["RasFreeEapUserIdentityA", "ras/RasFreeEapUserIdentityA"]
old-location: rras\rasfreeeapuseridentity.htm
tech.root: RRAS
ms.assetid: 84102fdc-b44a-415e-b67e-58c82e662a23
ms.date: 12/05/2018
ms.keywords: RasFreeEapUserIdentity, RasFreeEapUserIdentity function [RAS], RasFreeEapUserIdentityA, RasFreeEapUserIdentityW, _ras_rasfreeeapuseridentity, ras/RasFreeEapUserIdentity, ras/RasFreeEapUserIdentityA, ras/RasFreeEapUserIdentityW, rras.rasfreeeapuseridentity
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasFreeEapUserIdentityW (Unicode) and RasFreeEapUserIdentityA (ANSI)
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
 - RasFreeEapUserIdentityA
 - ras/RasFreeEapUserIdentityA
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
 - RasFreeEapUserIdentity
 - RasFreeEapUserIdentityA
 - RasFreeEapUserIdentityW
---

# RasFreeEapUserIdentityA function


## -description

Use the 
<b>RasFreeEapUserIdentity</b> function to free the memory buffer returned by 
<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a>.

## -parameters

### -param pRasEapUserIdentity [in]

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa377247(v=vs.85)">RASEAPUSERIDENTITY</a> structure returned by the 
<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a> function. 
<b>RasFreeEapUserIdentity</b> frees the memory occupied by this structure.

## -remarks

<b>RasFreeEapUserIdentity</b> can be called with the <i>pRasEapUserIdentity</i> parameter equal to <b>NULL</b>.





> [!NOTE]
> The ras.h header defines RasFreeEapUserIdentity as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377247(v=vs.85)">RASEAPUSERIDENTITY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a>
