---
UID: NF:mfapi.MFGetTimerPeriodicity
title: MFGetTimerPeriodicity function (mfapi.h)
description: Retrieves the timer interval for the MFAddPeriodicCallback function.
helpviewer_keywords: ["19d7ae7e-7ae3-474d-8111-3b60b9adb918","MFGetTimerPeriodicity","MFGetTimerPeriodicity function [Media Foundation]","mf.mfgettimerperiodicity","mfapi/MFGetTimerPeriodicity"]
old-location: mf\mfgettimerperiodicity.htm
tech.root: mf
ms.assetid: 19d7ae7e-7ae3-474d-8111-3b60b9adb918
ms.date: 12/05/2018
ms.keywords: 19d7ae7e-7ae3-474d-8111-3b60b9adb918, MFGetTimerPeriodicity, MFGetTimerPeriodicity function [Media Foundation], mf.mfgettimerperiodicity, mfapi/MFGetTimerPeriodicity
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetTimerPeriodicity
 - mfapi/MFGetTimerPeriodicity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFGetTimerPeriodicity
---

# MFGetTimerPeriodicity function


## -description

Retrieves the timer interval for the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback">MFAddPeriodicCallback</a> function.

## -parameters

### -param Periodicity [out]

Receives the timer interval, in milliseconds.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>