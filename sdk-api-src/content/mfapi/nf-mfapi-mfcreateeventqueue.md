---
UID: NF:mfapi.MFCreateEventQueue
title: MFCreateEventQueue function (mfapi.h)
description: Creates an event queue.
helpviewer_keywords: ["214cea99-37cf-4571-aa00-7b3e220a6b84","MFCreateEventQueue","MFCreateEventQueue function [Media Foundation]","mf.mfcreateeventqueue","mfapi/MFCreateEventQueue"]
old-location: mf\mfcreateeventqueue.htm
tech.root: mf
ms.assetid: 214cea99-37cf-4571-aa00-7b3e220a6b84
ms.date: 12/05/2018
ms.keywords: 214cea99-37cf-4571-aa00-7b3e220a6b84, MFCreateEventQueue, MFCreateEventQueue function [Media Foundation], mf.mfcreateeventqueue, mfapi/MFCreateEventQueue
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
 - MFCreateEventQueue
 - mfapi/MFCreateEventQueue
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
 - MFCreateEventQueue
---

# MFCreateEventQueue function


## -description

Creates an event queue.

## -parameters

### -param ppMediaEventQueue

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue">IMFMediaEventQueue</a> interface of the event queue. The caller must release the interface.

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

This function creates a helper object that you can use to implement the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> interface.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-event-generators">Media Event Generators</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>