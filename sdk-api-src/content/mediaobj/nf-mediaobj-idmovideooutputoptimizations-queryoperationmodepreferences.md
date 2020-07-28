---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.QueryOperationModePreferences
title: IDMOVideoOutputOptimizations::QueryOperationModePreferences (mediaobj.h)
description: The QueryOperationModePreferences method retrieves the DMO's preferred optimization features.
helpviewer_keywords: ["IDMOVideoOutputOptimizations interface [DirectShow]","QueryOperationModePreferences method","IDMOVideoOutputOptimizations.QueryOperationModePreferences","IDMOVideoOutputOptimizations::QueryOperationModePreferences","IDMOVideoOutputOptimizationsQueryOperationModePreferences","QueryOperationModePreferences","QueryOperationModePreferences method [DirectShow]","QueryOperationModePreferences method [DirectShow]","IDMOVideoOutputOptimizations interface","dshow.idmovideooutputoptimizations_queryoperationmodepreferences","mediaobj/IDMOVideoOutputOptimizations::QueryOperationModePreferences"]
old-location: dshow\idmovideooutputoptimizations_queryoperationmodepreferences.htm
tech.root: dshow
ms.assetid: 55916330-8395-4952-a349-f1ab5a3a2d64
ms.date: 12/05/2018
ms.keywords: IDMOVideoOutputOptimizations interface [DirectShow],QueryOperationModePreferences method, IDMOVideoOutputOptimizations.QueryOperationModePreferences, IDMOVideoOutputOptimizations::QueryOperationModePreferences, IDMOVideoOutputOptimizationsQueryOperationModePreferences, QueryOperationModePreferences, QueryOperationModePreferences method [DirectShow], QueryOperationModePreferences method [DirectShow],IDMOVideoOutputOptimizations interface, dshow.idmovideooutputoptimizations_queryoperationmodepreferences, mediaobj/IDMOVideoOutputOptimizations::QueryOperationModePreferences
f1_keywords:
- mediaobj/IDMOVideoOutputOptimizations.QueryOperationModePreferences
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dmoguids.lib
- Dmoguids.dll
api_name:
- IDMOVideoOutputOptimizations.QueryOperationModePreferences
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMOVideoOutputOptimizations::QueryOperationModePreferences


## -description



The <code>QueryOperationModePreferences</code> method retrieves the DMO's preferred optimization features.




## -parameters




### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param pdwRequestedCapabilities

Pointer to a variable that receives the DMO's requested features. The returned value is a bitwise combination of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_video_output_stream_flags">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-idmovideooutputoptimizations">IDMOVideoOutputOptimizations Interface</a>
 

 

