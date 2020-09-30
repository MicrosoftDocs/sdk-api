---
UID: NC:ras.RasCustomHangUpFn
title: RasCustomHangUpFn (ras.h)
description: The RasCustomHangUp function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom connection hang-up routines.
helpviewer_keywords: ["RasCustomHangUp","RasCustomHangUp callback function [RAS]","RasCustomHangUpFn","RasCustomHangUpFn callback","_ras_rascustomhangup","ras/RasCustomHangUp","rras.rascustomhangup"]
old-location: rras\rascustomhangup.htm
tech.root: RRAS
ms.assetid: 56410af3-7b23-4536-998d-88d78d45585d
ms.date: 12/05/2018
ms.keywords: RasCustomHangUp, RasCustomHangUp callback function [RAS], RasCustomHangUpFn, RasCustomHangUpFn callback, _ras_rascustomhangup, ras/RasCustomHangUp, rras.rascustomhangup
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
 - RasCustomHangUpFn
 - ras/RasCustomHangUpFn
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
 - RasCustomHangUp
---

# RasCustomHangUpFn callback function


## -description

The 
<b>RasCustomHangUp</b> function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom connection hang-up routines.

## -parameters

### -param hRasConn

Handle to the RAS connection to hang up.

## -returns

If the function succeeds, the return value should be <b>ERROR_SUCCESS</b>.

If the function fails, the return value should be a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -remarks

RAS  calls this entry point from 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>, if the <b>szCustomDialDll</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure for the entry being dialed specifies a custom-dialing DLL.

## -see-also

<a href="/windows/desktop/RRAS/custom-dialers">Custom Dialers</a>



<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomdialfn">RasCustomDial</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomdialdlgfn">RasCustomDialDlg</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomentrydlgfn">RasCustomEntryDlg</a>



<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>