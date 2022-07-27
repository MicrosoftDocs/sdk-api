---
UID: NF:mfapi.MFUnlockWorkQueue
title: MFUnlockWorkQueue function (mfapi.h)
description: Unlocks a work queue. (MFUnlockWorkQueue)
helpviewer_keywords: ["MFUnlockWorkQueue","MFUnlockWorkQueue function [Media Foundation]","bbc22fa7-b4d7-47b2-b065-099fbb2ed092","mf.mfunlockworkqueue","mfapi/MFUnlockWorkQueue"]
old-location: mf\mfunlockworkqueue.htm
tech.root: mf
ms.assetid: bbc22fa7-b4d7-47b2-b065-099fbb2ed092
ms.date: 12/05/2018
ms.keywords: MFUnlockWorkQueue, MFUnlockWorkQueue function [Media Foundation], bbc22fa7-b4d7-47b2-b065-099fbb2ed092, mf.mfunlockworkqueue, mfapi/MFUnlockWorkQueue
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFUnlockWorkQueue
 - mfapi/MFUnlockWorkQueue
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
 - MFUnlockWorkQueue
---

# MFUnlockWorkQueue function


## -description

Unlocks a work queue.

## -parameters

### -param dwWorkQueue [in]

Identifier for the work queue to be unlocked. The identifier is returned by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function.

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

The application must call <b>MFUnlockWorkQueue</b> once for every call to <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> and then once for every call to <a href="/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue">MFLockWorkQueue</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
