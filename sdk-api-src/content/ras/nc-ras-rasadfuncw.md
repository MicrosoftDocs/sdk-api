---
UID: NC:ras.RASADFUNCW
title: RASADFUNCW (ras.h)
description: The RASADFunc function is an application-defined callback function that is used to provide a customized user interface for autodialing. (Unicode)
helpviewer_keywords: ["RASADFunc","RASADFunc callback","RASADFunc callback function [RAS]","RASADFuncA","RASADFuncW","_ras_rasadfunc","ras/RASADFunc","ras/RASADFuncA","ras/RASADFuncW","rras.rasadfunc"]
old-location: rras\rasadfunc.htm
tech.root: RRAS
ms.assetid: e014624a-1ee1-4de3-ba59-cd090b3fa711
ms.date: 12/05/2018
ms.keywords: RASADFunc, RASADFunc callback, RASADFunc callback function [RAS], RASADFuncA, RASADFuncW, _ras_rasadfunc, ras/RASADFunc, ras/RASADFuncA, ras/RASADFuncW, rras.rasadfunc
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RASADFuncW (Unicode) and RASADFuncA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RASADFUNCW
 - ras/RASADFUNCW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RASADFunc
 - RASADFuncA
 - RASADFuncW
---

# RASADFUNCW callback function


## -description

The 
<b>RASADFunc</b> function is an application-defined callback function that is used to provide a customized user interface for autodialing.

## -parameters

### -param unnamedParam1

### -param unnamedParam2

### -param unnamedParam3

### -param unnamedParam4

#### - lpAutoDialParams [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)">RASADPARAMS</a> structure that indicates how to position the window of the AutoDial user interface. The structure can also specify a parent window for the AutoDial window.


#### - lpdwRetCode [out]

Pointer to a variable that receives a value if the function performs the dialing operation. If the dialing operation succeeds, set this variable to <b>ERROR_SUCCESS</b>. If the dialing operation fails, set it to a nonzero value.


#### - lpszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies the phone-book entry to use.


#### - lpszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 




<b>Windows Me/98/95:  </b>This parameter is always <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.

## -returns

If the application performs the dialing operation, return <b>TRUE</b>. Use the <i>lpdwRetCode</i> parameter to indicate the results of the dialing operation.

If the application does not perform the dialing operation, return <b>FALSE</b>. In this case, the system uses the default user interface for dialing.

## -remarks

When the system starts an AutoDial operation for a phone-book entry with a custom AutoDial handler, it calls the specified 
<b>RASADFunc</b>. The 
<b>RASADFunc</b> can start a thread to perform the custom-dialing operation. The 
<b>RASADFunc</b> function returns <b>TRUE</b> to indicate that it took over the dialing, or <b>FALSE</b> to allow the system to perform the dialing.

If the 
<b>RASADFunc</b> function performs the dialing operation, it presents its own user interface for dialing and calls the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function to do the actual dialing. The 
<b>RASADFunc</b> then returns <b>TRUE</b> to indicate that it took over the dialing. When the dialing operation has been completed, set the variable pointed to by the <i>lpdwRetCode</i> parameter to indicate success or failure.

The AutoDial DLL must provide both a <b>RASADFUNCA</b> (ANSI) and a <b>RASADFUNCW</b> (Unicode) version of the 
<b>RASADFunc</b> handler. To enable a 
<b>RASADFunc</b> AutoDial handler for a phone-book entry, use the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure in a call to the 
<a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a> function. The <b>szAutodialDll</b> member specifies the name of the DLL that contains the handler, and the <b>szAutodialFunc</b> member specifies the exported name of the handler. The <b>szAutodialFunc</b> member should not include the "A" or "W" suffix.

<b>RASADFunc</b> is a placeholder for the library-defined function name. The <b>RASADFUNC</b> type is a pointer to a 
<b>RASADFunc</b> function.





> [!NOTE]
> The ras.h header defines RASADFUNC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
