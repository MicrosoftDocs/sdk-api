---
UID: NF:ras.RasSetAutodialEnableA
title: RasSetAutodialEnableA function (ras.h)
description: The RasSetAutodialEnable function enables or disables the AutoDial feature for a specified TAPI dialing location. (ANSI)
helpviewer_keywords: ["RasSetAutodialEnableA", "ras/RasSetAutodialEnableA"]
old-location: rras\rassetautodialenable.htm
tech.root: RRAS
ms.assetid: 0d5f7b8e-9bce-4e72-8657-f465ce4008c4
ms.date: 12/05/2018
ms.keywords: RasSetAutodialEnable, RasSetAutodialEnable function [RAS], RasSetAutodialEnableA, RasSetAutodialEnableW, _ras_rassetautodialenable, ras/RasSetAutodialEnable, ras/RasSetAutodialEnableA, ras/RasSetAutodialEnableW, rras.rassetautodialenable
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetAutodialEnableW (Unicode) and RasSetAutodialEnableA (ANSI)
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
 - RasSetAutodialEnableA
 - ras/RasSetAutodialEnableA
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
 - RasSetAutodialEnable
 - RasSetAutodialEnableA
 - RasSetAutodialEnableW
---

# RasSetAutodialEnableA function


## -description

The 
<b>RasSetAutodialEnable</b> function enables or disables the AutoDial feature for a specified TAPI dialing location. For more information about TAPI dialing locations, see  <a href="/windows/desktop/Tapi/telephony-application-programming-interfaces">Telephony Application Programming Interfaces (TAPI)</a>  in the Platform Software Development Kit (SDK).

## -parameters

### -param unnamedParam1 [in]

Specifies the identifier of a TAPI dialing location.

### -param unnamedParam2 [in]

Specifies <b>TRUE</b> to enable AutoDial for the dialing location indicated by the <i>dwDialingLocation</i> parameter. Specifies <b>FALSE</b> to disable it.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a non-zero error code from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rasgetautodialenablea">RasGetAutodialEnable</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>

## -remarks

> [!NOTE]
> The ras.h header defines RasSetAutodialEnable as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
