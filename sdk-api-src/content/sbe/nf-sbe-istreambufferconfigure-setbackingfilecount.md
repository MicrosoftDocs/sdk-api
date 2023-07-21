---
UID: NF:sbe.IStreamBufferConfigure.SetBackingFileCount
title: IStreamBufferConfigure::SetBackingFileCount (sbe.h)
description: The SetBackingFileCount method sets the maximum and minimum number of backing files.
helpviewer_keywords: ["IStreamBufferConfigure interface [Microsoft TV Technologies]","SetBackingFileCount method","IStreamBufferConfigure.SetBackingFileCount","IStreamBufferConfigure::SetBackingFileCount","IStreamBufferConfigureSetBackingFileCount","SetBackingFileCount","SetBackingFileCount method [Microsoft TV Technologies]","SetBackingFileCount method [Microsoft TV Technologies]","IStreamBufferConfigure interface","mstv.istreambufferconfigure_setbackingfilecount","sbe/IStreamBufferConfigure::SetBackingFileCount"]
old-location: mstv\istreambufferconfigure_setbackingfilecount.htm
tech.root: mstv
ms.assetid: c984ec40-22d0-4670-af7e-3c2ce611850f
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure interface [Microsoft TV Technologies],SetBackingFileCount method, IStreamBufferConfigure.SetBackingFileCount, IStreamBufferConfigure::SetBackingFileCount, IStreamBufferConfigureSetBackingFileCount, SetBackingFileCount, SetBackingFileCount method [Microsoft TV Technologies], SetBackingFileCount method [Microsoft TV Technologies],IStreamBufferConfigure interface, mstv.istreambufferconfigure_setbackingfilecount, sbe/IStreamBufferConfigure::SetBackingFileCount
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IStreamBufferConfigure::SetBackingFileCount
 - sbe/IStreamBufferConfigure::SetBackingFileCount
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
 - IStreamBufferConfigure.SetBackingFileCount
---

# IStreamBufferConfigure::SetBackingFileCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetBackingFileCount</b> method sets the maximum and minimum number of backing files.

## -parameters

### -param dwMin [in]

Specifies the backing file minimum. The valid range is from 4 to 100.

### -param dwMax [in]

Specifies the backing file maximum. The valid range is from 6 to 102, and the value must be at least 2 greater than <i>dwMin</i>.

## -returns

Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object was not initialized.

</td>
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

If the reader lags behind the writer by more than <i>dwMin</i> files, the writer starts to send STREAMBUFFER_EC_CONTENT_BECOMING_STALE events. If the reader lags behind the writer by more than <i>dwMax</i> files, the writer begins to overwrite files and sends an STREAMBUFFER_EC_STALE_FILE_DELETED event.

Before calling this method, call <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferinitialize-sethkey">IStreamBufferInitialize::SetHKEY</a> to specify a registry key where the information will be stored.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure">IStreamBufferConfigure Interface</a>