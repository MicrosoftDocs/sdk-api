---
UID: NF:mfapi.MFRemovePeriodicCallback
title: MFRemovePeriodicCallback function (mfapi.h)
description: Cancels a callback function that was set by the MFAddPeriodicCallback function.
helpviewer_keywords: ["MFRemovePeriodicCallback","MFRemovePeriodicCallback function [Media Foundation]","e70cdad3-c330-4368-8ef8-d616157b5e72","mf.mfremoveperiodiccallback","mfapi/MFRemovePeriodicCallback"]
old-location: mf\mfremoveperiodiccallback.htm
tech.root: mf
ms.assetid: e70cdad3-c330-4368-8ef8-d616157b5e72
ms.date: 12/05/2018
ms.keywords: MFRemovePeriodicCallback, MFRemovePeriodicCallback function [Media Foundation], e70cdad3-c330-4368-8ef8-d616157b5e72, mf.mfremoveperiodiccallback, mfapi/MFRemovePeriodicCallback
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
 - MFRemovePeriodicCallback
 - mfapi/MFRemovePeriodicCallback
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
 - MFRemovePeriodicCallback
---

# MFRemovePeriodicCallback function


## -description

Cancels a callback function that was set by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback">MFAddPeriodicCallback</a> function.

## -parameters

### -param dwKey [in]

Key that identifies the callback. This value is retrieved by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback">MFAddPeriodicCallback</a> function.

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

The callback is dispatched on another thread, and this function does not attempt to synchronize with the callback thread. Therefore, it is possible for the callback to be invoked after this function returns.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>