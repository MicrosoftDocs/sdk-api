---
UID: NF:mfidl.IMFTimer.CancelTimer
title: IMFTimer::CancelTimer (mfidl.h)
description: Cancels a timer that was set using the IMFTimer::SetTimer method.
helpviewer_keywords: ["3fa65809-1652-4903-92ad-1034bcdf0743","CancelTimer","CancelTimer method [Media Foundation]","CancelTimer method [Media Foundation]","IMFTimer interface","IMFTimer interface [Media Foundation]","CancelTimer method","IMFTimer.CancelTimer","IMFTimer::CancelTimer","mf.imftimer_canceltimer","mfidl/IMFTimer::CancelTimer"]
old-location: mf\imftimer_canceltimer.htm
tech.root: mf
ms.assetid: 3fa65809-1652-4903-92ad-1034bcdf0743
ms.date: 12/05/2018
ms.keywords: 3fa65809-1652-4903-92ad-1034bcdf0743, CancelTimer, CancelTimer method [Media Foundation], CancelTimer method [Media Foundation],IMFTimer interface, IMFTimer interface [Media Foundation],CancelTimer method, IMFTimer.CancelTimer, IMFTimer::CancelTimer, mf.imftimer_canceltimer, mfidl/IMFTimer::CancelTimer
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimer::CancelTimer
 - mfidl/IMFTimer::CancelTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTimer.CancelTimer
---

# IMFTimer::CancelTimer


## -description

Cancels a timer that was set using the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftimer-settimer">IMFTimer::SetTimer</a> method.

## -parameters

### -param punkKey [in]

Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppunkKey</i> parameter of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftimer-settimer">SetTimer</a> method.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

Because the timer is dispatched asynchronously, the application's timer callback might get invoked even if this method succeeds.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer">IMFTimer</a>