---
UID: NF:dciman.DCICloseProvider
title: DCICloseProvider function (dciman.h)
description: Closes a device context of a display.
helpviewer_keywords: ["DCICloseProvider","DCICloseProvider function [Windows API]","_dciman_dcicloseprovider","dciman/DCICloseProvider","winprog._dciman_dcicloseprovider","winui._dciman_dcicloseprovider"]
old-location: winprog\_dciman_dcicloseprovider.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dcicloseprovider.htm
ms.date: 12/05/2018
ms.keywords: DCICloseProvider, DCICloseProvider function [Windows API], _dciman_dcicloseprovider, dciman/DCICloseProvider, winprog._dciman_dcicloseprovider, winui._dciman_dcicloseprovider
req.header: dciman.h
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
req.lib: Dciman32.lib
req.dll: Dciman32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCICloseProvider
 - dciman/DCICloseProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dciman32.dll
api_name:
 - DCICloseProvider
---

# DCICloseProvider function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Closes a device context of a display.

## -parameters

### -param hdc [in]

The device context handle to be closed.  The handle was created with <a href="/windows/desktop/api/dciman/nf-dciman-dciopenprovider">DCIOpenProvider</a>.

## -returns

If the function succeeds, the return value is nonzero.  Otherwise, it returns zero.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>