---
UID: NF:ras.RasGetAutodialEnableA
title: RasGetAutodialEnableA function (ras.h)
description: The RasGetAutodialEnable function indicates whether the AutoDial feature is enabled for a specified TAPI dialing location. (ANSI)
helpviewer_keywords: ["RasGetAutodialEnableA", "ras/RasGetAutodialEnableA"]
old-location: rras\rasgetautodialenable.htm
tech.root: RRAS
ms.assetid: 221f91e6-86bd-4450-92c8-ec3290712c18
ms.date: 12/05/2018
ms.keywords: RasGetAutodialEnable, RasGetAutodialEnable function [RAS], RasGetAutodialEnableA, RasGetAutodialEnableW, _ras_rasgetautodialenable, ras/RasGetAutodialEnable, ras/RasGetAutodialEnableA, ras/RasGetAutodialEnableW, rras.rasgetautodialenable
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetAutodialEnableW (Unicode) and RasGetAutodialEnableA (ANSI)
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
 - RasGetAutodialEnableA
 - ras/RasGetAutodialEnableA
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
 - RasGetAutodialEnable
 - RasGetAutodialEnableA
 - RasGetAutodialEnableW
---

# RasGetAutodialEnableA function


## -description

The 
<b>RasGetAutodialEnable</b> function indicates whether the AutoDial feature is enabled for a specified TAPI dialing location. For more information about TAPI dialing locations, see the <a href="/windows/desktop/Tapi/telephony-application-programming-interfaces">TAPI Programmer's Reference</a> in the Platform Software Development Kit (SDK).

## -parameters

### -param unnamedParam1 [in]

Specifies the identifier of a TAPI dialing location.

### -param unnamedParam2 [out]

Pointer to a BOOL variable that receives a nonzero value if AutoDial is enabled for the specified dialing location, or zero if it is not enabled.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rassetautodialenablea">RasSetAutodialEnable</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>

## -remarks

> [!NOTE]
> The ras.h header defines RasGetAutodialEnable as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
