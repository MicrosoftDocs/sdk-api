---
UID: NC:pdh.CounterPathCallBack
title: CounterPathCallBack (pdh.h)
description: Applications implement the CounterPathCallBack function to process the counter path strings returned by the Browse dialog box.
helpviewer_keywords: ["CounterPathCallBack","CounterPathCallBack callback","CounterPathCallBack callback function [Perf]","_win32_counterpathcallback","base.counterpathcallback","pdh/CounterPathCallBack","perf.counterpathcallback"]
old-location: perf\counterpathcallback.htm
tech.root: perf
ms.assetid: b7a2112e-9f50-4a36-b022-f9609b2827bc
ms.date: 12/05/2018
ms.keywords: CounterPathCallBack, CounterPathCallBack callback, CounterPathCallBack callback function [Perf], _win32_counterpathcallback, base.counterpathcallback, pdh/CounterPathCallBack, perf.counterpathcallback
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CounterPathCallBack
 - pdh/CounterPathCallBack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Pdh.h
api_name:
 - CounterPathCallBack
---

# CounterPathCallBack callback function


## -description

Applications implement the <b>CounterPathCallBack</b> function to process the counter path strings returned by the  <b>Browse</b> dialog box.

## -parameters

### -param unnamedParam1

User-defined value passed to the callback function by the <b>Browse</b> dialog box. You set this value in the <b>dwCallBackArg</b> member of the 
<a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a">PDH_BROWSE_DLG_CONFIG</a> structure.


## -returns

Return ERROR_SUCCESS if the function succeeds. 

If the function fails due to a transient error, you can return PDH_RETRY and PDH will call your callback immediately.

Otherwise, return an appropriate error code. The error code is passed back to the caller of <a href="/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersa">PdhBrowseCounters</a>.

## -remarks

The following members of the 
<a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a">PDH_BROWSE_DLG_CONFIG</a> structure are used to communicate with the callback function:

## -see-also

<a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a">PDH_BROWSE_DLG_CONFIG</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersa">PdhBrowseCounters</a>