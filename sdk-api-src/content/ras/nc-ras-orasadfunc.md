---
UID: NC:ras.ORASADFUNC
title: ORASADFUNC (ras.h)
description: The ORASADFunc function is an application-defined callback function that is used to provide a customized user interface for autodialing.
helpviewer_keywords: ["ORASADFunc","ORASADFunc callback","ORASADFunc callback function [RAS]","_ras_orasadfunc","ras/ORASADFunc","rras.orasadfunc"]
old-location: rras\orasadfunc.htm
tech.root: RRAS
ms.assetid: d3ad49e3-6807-419d-8d05-f703f5327020
ms.date: 12/05/2018
ms.keywords: ORASADFunc, ORASADFunc callback, ORASADFunc callback function [RAS], _ras_orasadfunc, ras/ORASADFunc, rras.orasadfunc
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ORASADFUNC
 - ras/ORASADFUNC
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
 - ORASADFunc
---

# ORASADFUNC callback function


## -description

The 
<b>ORASADFunc</b> function is an application-defined callback function that is used to provide a customized user interface for autodialing.

This prototype is provided for compatibility with earlier versions of Windows. New applications should use the 
<a href="/windows/desktop/api/ras/nc-ras-rasadfunca">RASADFunc</a> callback function. Support for this prototype may be removed in future versions of RAS.

## -parameters

### -param unnamedParam1

### -param unnamedParam2

### -param unnamedParam3

### -param unnamedParam4

#### - dwFlags [in]

Reserved; must be zero.


#### - hwndOwner [in]

Handle of the owner window.


#### - lpdwRetCode [in]

Pointer to a variable that the callback function fills in with the results of the dialing operation. If the dialing operation succeeds, set this variable to ERROR_SUCCESS. If the dialing operation fails, set it to a nonzero value.


#### - lpszEntry [in]

Pointer to a null-terminated string that specifies the phone-book entry to use.

## -returns

If the callback function performs the dialing operation, return <b>TRUE</b>. Use the <i>lpdwRetCode</i> parameter to indicate the results of the dialing operation.

If the callback function does not perform the dialing operation, return <b>FALSE</b>. In this case, the system uses the default user interface for dialing.

## -remarks

If the 
<b>ORASADFunc</b> function performs the dialing operation, it presents its own user interface for dialing and calls the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function to do the actual dialing. The 
<b>ORASADFunc</b> then returns <b>TRUE</b> to indicate that it took over the dialing. When the dialing operation has been completed, set the variable pointed to by <i>lpdwRetCode</i> to indicate success or failure.

To enable an 
<b>ORASADFunc</b> handler for a phone-book entry, use the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure in a call to the 
<a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a> function. The <b>szAutodialDll</b> member specifies the name of the DLL that contains the handler, and the <b>szAutodialDll</b> member specifies the exported name of the handler.

The 
<b>ORASADFunc</b> function is a placeholder for the library-defined function name. The <b>ORASADFUNC</b> type is a pointer to an 
<b>ORASADFunc</b> function.

## -see-also

<a href="/windows/desktop/api/ras/nc-ras-rasadfunca">RASADFunc</a>



<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>