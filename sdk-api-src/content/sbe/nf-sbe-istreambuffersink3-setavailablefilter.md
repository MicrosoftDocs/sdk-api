---
UID: NF:sbe.IStreamBufferSink3.SetAvailableFilter
title: IStreamBufferSink3::SetAvailableFilter (sbe.h)
description: The SetAvailableFilter method limits how far the Stream Buffer Source filter can seek backward, relative to the current recording position.
helpviewer_keywords: ["IStreamBufferSink3 interface [Microsoft TV Technologies]","SetAvailableFilter method","IStreamBufferSink3.SetAvailableFilter","IStreamBufferSink3::SetAvailableFilter","IStreamBufferSink3SetAvailableFilter","SetAvailableFilter","SetAvailableFilter method [Microsoft TV Technologies]","SetAvailableFilter method [Microsoft TV Technologies]","IStreamBufferSink3 interface","mstv.istreambuffersink3_setavailablefilter","sbe/IStreamBufferSink3::SetAvailableFilter"]
old-location: mstv\istreambuffersink3_setavailablefilter.htm
tech.root: mstv
ms.assetid: 81822768-f627-4324-815f-51d06b4bd7b3
ms.date: 12/05/2018
ms.keywords: IStreamBufferSink3 interface [Microsoft TV Technologies],SetAvailableFilter method, IStreamBufferSink3.SetAvailableFilter, IStreamBufferSink3::SetAvailableFilter, IStreamBufferSink3SetAvailableFilter, SetAvailableFilter, SetAvailableFilter method [Microsoft TV Technologies], SetAvailableFilter method [Microsoft TV Technologies],IStreamBufferSink3 interface, mstv.istreambuffersink3_setavailablefilter, sbe/IStreamBufferSink3::SetAvailableFilter
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IStreamBufferSink3::SetAvailableFilter
 - sbe/IStreamBufferSink3::SetAvailableFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferSink3.SetAvailableFilter
---

# IStreamBufferSink3::SetAvailableFilter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetAvailableFilter</b> method limits how far the Stream Buffer Source filter can seek backward, relative to the current recording position.

## -parameters

### -param prtMin [in, out]

On input, specifies the earliest seek time, in 100-nanosecond units, relative to the recording position when the method is called. The value must be less than or equal to zero. To make the entire backing store available, use the value -MAXLONGLONG.

On output, this parameter receives the actual minimum seek time. The two values may differ if the requested time exceeds the amount of time that is available.

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

The minimum seek time is an absolute position within the file. For example, suppose the value is -50000000. Immediately after the method returns, the Stream Buffer Source filter can seek backward 5 seconds, but no further. After another 15 seconds of recording, the filter can seek backward 20 seconds from the new position.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersink3">IStreamBufferSink3 Interface</a>