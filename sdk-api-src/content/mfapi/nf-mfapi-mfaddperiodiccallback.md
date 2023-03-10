---
UID: NF:mfapi.MFAddPeriodicCallback
title: MFAddPeriodicCallback function (mfapi.h)
description: Sets a callback function to be called at a fixed interval. (MFAddPeriodicCallback)
helpviewer_keywords: ["MFAddPeriodicCallback","MFAddPeriodicCallback function [Media Foundation]","e5898fc8-72e9-45cc-8e85-4410ed7cc512","mf.mfaddperiodiccallback","mfapi/MFAddPeriodicCallback"]
old-location: mf\mfaddperiodiccallback.htm
tech.root: mf
ms.assetid: e5898fc8-72e9-45cc-8e85-4410ed7cc512
ms.date: 12/05/2018
ms.keywords: MFAddPeriodicCallback, MFAddPeriodicCallback function [Media Foundation], e5898fc8-72e9-45cc-8e85-4410ed7cc512, mf.mfaddperiodiccallback, mfapi/MFAddPeriodicCallback
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
 - MFAddPeriodicCallback
 - mfapi/MFAddPeriodicCallback
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
 - MFAddPeriodicCallback
---

# MFAddPeriodicCallback function


## -description

Sets a callback function to be called at a fixed interval.

## -parameters

### -param Callback [in]

Pointer to the callback function, of type <a href="/windows/desktop/api/mfapi/nc-mfapi-mfperiodiccallback">MFPERIODICCALLBACK</a>.

### -param pContext [in]

Pointer to a caller-provided object that implements <b>IUnknown</b>, or <b>NULL</b>. This parameter is passed to the callback function.

### -param pdwKey [out]

Receives a key that can be used to cancel the callback. To cancel the callback, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback">MFRemovePeriodicCallback</a> and pass this key as the <i>dwKey</i> parameter.

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

## -remarks

To get the timer interval for the periodic callback, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity">MFGetTimerPeriodicity</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
