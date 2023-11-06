---
UID: NF:sbe.IStreamBufferConfigure.SetBackingFileDuration
title: IStreamBufferConfigure::SetBackingFileDuration (sbe.h)
description: The SetBackingFileDuration method sets the duration of all backing files.
helpviewer_keywords: ["IStreamBufferConfigure interface [Microsoft TV Technologies]","SetBackingFileDuration method","IStreamBufferConfigure.SetBackingFileDuration","IStreamBufferConfigure::SetBackingFileDuration","IStreamBufferConfigureSetBackingFileDuration","SetBackingFileDuration","SetBackingFileDuration method [Microsoft TV Technologies]","SetBackingFileDuration method [Microsoft TV Technologies]","IStreamBufferConfigure interface","mstv.istreambufferconfigure_setbackingfileduration","sbe/IStreamBufferConfigure::SetBackingFileDuration"]
old-location: mstv\istreambufferconfigure_setbackingfileduration.htm
tech.root: mstv
ms.assetid: 1825896e-0e3c-4b89-8e0e-59faa0f8000d
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure interface [Microsoft TV Technologies],SetBackingFileDuration method, IStreamBufferConfigure.SetBackingFileDuration, IStreamBufferConfigure::SetBackingFileDuration, IStreamBufferConfigureSetBackingFileDuration, SetBackingFileDuration, SetBackingFileDuration method [Microsoft TV Technologies], SetBackingFileDuration method [Microsoft TV Technologies],IStreamBufferConfigure interface, mstv.istreambufferconfigure_setbackingfileduration, sbe/IStreamBufferConfigure::SetBackingFileDuration
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
 - IStreamBufferConfigure::SetBackingFileDuration
 - sbe/IStreamBufferConfigure::SetBackingFileDuration
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
 - IStreamBufferConfigure.SetBackingFileDuration
---

# IStreamBufferConfigure::SetBackingFileDuration


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetBackingFileDuration</b> method sets the duration of all backing files.

## -parameters

### -param dwSeconds [in]

Specifies the file duration, in seconds. The minimum value is 15.

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

Before calling this method, call <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferinitialize-sethkey">IStreamBufferInitialize::SetHKEY</a> to specify a registry key where the information will be stored.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure">IStreamBufferConfigure Interface</a>