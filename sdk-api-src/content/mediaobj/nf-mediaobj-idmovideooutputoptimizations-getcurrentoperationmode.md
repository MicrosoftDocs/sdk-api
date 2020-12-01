---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.GetCurrentOperationMode
title: IDMOVideoOutputOptimizations::GetCurrentOperationMode (mediaobj.h)
description: The GetCurrentOperationMode method retrieves the optimization features in effect.
helpviewer_keywords: ["GetCurrentOperationMode","GetCurrentOperationMode method [DirectShow]","GetCurrentOperationMode method [DirectShow]","IDMOVideoOutputOptimizations interface","IDMOVideoOutputOptimizations interface [DirectShow]","GetCurrentOperationMode method","IDMOVideoOutputOptimizations.GetCurrentOperationMode","IDMOVideoOutputOptimizations::GetCurrentOperationMode","IDMOVideoOutputOptimizationsGetCurrentOperationMode","dshow.idmovideooutputoptimizations_getcurrentoperationmode","mediaobj/IDMOVideoOutputOptimizations::GetCurrentOperationMode"]
old-location: dshow\idmovideooutputoptimizations_getcurrentoperationmode.htm
tech.root: dshow
ms.assetid: ddfc65ea-e336-40b8-a901-53ebc3ee7d86
ms.date: 12/05/2018
ms.keywords: GetCurrentOperationMode, GetCurrentOperationMode method [DirectShow], GetCurrentOperationMode method [DirectShow],IDMOVideoOutputOptimizations interface, IDMOVideoOutputOptimizations interface [DirectShow],GetCurrentOperationMode method, IDMOVideoOutputOptimizations.GetCurrentOperationMode, IDMOVideoOutputOptimizations::GetCurrentOperationMode, IDMOVideoOutputOptimizationsGetCurrentOperationMode, dshow.idmovideooutputoptimizations_getcurrentoperationmode, mediaobj/IDMOVideoOutputOptimizations::GetCurrentOperationMode
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMOVideoOutputOptimizations::GetCurrentOperationMode
 - mediaobj/IDMOVideoOutputOptimizations::GetCurrentOperationMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOVideoOutputOptimizations.GetCurrentOperationMode
---

# IDMOVideoOutputOptimizations::GetCurrentOperationMode


## -description

The <code>GetCurrentOperationMode</code> method retrieves the optimization features in effect.

## -parameters

### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.

### -param pdwEnabledFeatures

Pointer to a variable that receives the current features. The returned value is a bitwise combination of zero or more flags from the <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_video_output_stream_flags">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-idmovideooutputoptimizations">IDMOVideoOutputOptimizations Interface</a>