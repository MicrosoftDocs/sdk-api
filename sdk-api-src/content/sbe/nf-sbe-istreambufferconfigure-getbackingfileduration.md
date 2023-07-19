---
UID: NF:sbe.IStreamBufferConfigure.GetBackingFileDuration
title: IStreamBufferConfigure::GetBackingFileDuration (sbe.h)
description: The GetBackingFileDuration method retrieves the duration of each backing file.
helpviewer_keywords: ["GetBackingFileDuration","GetBackingFileDuration method [Microsoft TV Technologies]","GetBackingFileDuration method [Microsoft TV Technologies]","IStreamBufferConfigure interface","IStreamBufferConfigure interface [Microsoft TV Technologies]","GetBackingFileDuration method","IStreamBufferConfigure.GetBackingFileDuration","IStreamBufferConfigure::GetBackingFileDuration","IStreamBufferConfigureGetBackingFileDuration","mstv.istreambufferconfigure_getbackingfileduration","sbe/IStreamBufferConfigure::GetBackingFileDuration"]
old-location: mstv\istreambufferconfigure_getbackingfileduration.htm
tech.root: mstv
ms.assetid: 3d02d87f-b617-4d46-82b2-41eb4b160d0f
ms.date: 12/05/2018
ms.keywords: GetBackingFileDuration, GetBackingFileDuration method [Microsoft TV Technologies], GetBackingFileDuration method [Microsoft TV Technologies],IStreamBufferConfigure interface, IStreamBufferConfigure interface [Microsoft TV Technologies],GetBackingFileDuration method, IStreamBufferConfigure.GetBackingFileDuration, IStreamBufferConfigure::GetBackingFileDuration, IStreamBufferConfigureGetBackingFileDuration, mstv.istreambufferconfigure_getbackingfileduration, sbe/IStreamBufferConfigure::GetBackingFileDuration
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
 - IStreamBufferConfigure::GetBackingFileDuration
 - sbe/IStreamBufferConfigure::GetBackingFileDuration
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
 - IStreamBufferConfigure.GetBackingFileDuration
---

# IStreamBufferConfigure::GetBackingFileDuration


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetBackingFileDuration</b> method retrieves the duration of each backing file.

## -parameters

### -param pdwSeconds [out]

Pointer to a variable that receives the file duration, in seconds.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure">IStreamBufferConfigure Interface</a>