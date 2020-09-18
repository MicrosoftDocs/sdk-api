---
UID: NN:wmsdkidl.IWMReaderStreamClock
title: IWMReaderStreamClock (wmsdkidl.h)
description: The IWMReaderStreamClock interface provides access to the clock used by the reader.This interface exists for every reader object.
helpviewer_keywords: ["IWMReaderStreamClock","IWMReaderStreamClock interface [windows Media Format]","IWMReaderStreamClock interface [windows Media Format]","described","IWMReaderStreamClockInterface","wmformat.iwmreaderstreamclock","wmsdkidl/IWMReaderStreamClock"]
old-location: wmformat\iwmreaderstreamclock.htm
tech.root: wmformat
ms.assetid: 0f170b6d-fd93-4bf8-8a98-f2a80f03b380
ms.date: 12/05/2018
ms.keywords: IWMReaderStreamClock, IWMReaderStreamClock interface [windows Media Format], IWMReaderStreamClock interface [windows Media Format],described, IWMReaderStreamClockInterface, wmformat.iwmreaderstreamclock, wmsdkidl/IWMReaderStreamClock
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IWMReaderStreamClock
 - wmsdkidl/IWMReaderStreamClock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMReaderStreamClock
---

# IWMReaderStreamClock interface


## -description

The <b>IWMReaderStreamClock</b> interface provides access to the clock used by the reader.

This interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderStreamClock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderStreamClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderStreamClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderstreamclock-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the stream clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderstreamclock-killtimer">KillTimer</a>
</td>
<td align="left" width="63%">
Cancels a timer on the stream clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderstreamclock-settimer">SetTimer</a>
</td>
<td align="left" width="63%">
Sets a timer on the stream clock.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="/windows/desktop/wmformat/reader-object">Reader Object</a>.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>