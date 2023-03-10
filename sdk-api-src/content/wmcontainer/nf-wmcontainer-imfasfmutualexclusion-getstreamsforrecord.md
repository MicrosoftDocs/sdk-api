---
UID: NF:wmcontainer.IMFASFMutualExclusion.GetStreamsForRecord
title: IMFASFMutualExclusion::GetStreamsForRecord (wmcontainer.h)
description: Retrieves the stream numbers contained in a record in the Advanced Systems Format mutual exclusion object.
helpviewer_keywords: ["GetStreamsForRecord","GetStreamsForRecord method [Media Foundation]","GetStreamsForRecord method [Media Foundation]","IMFASFMutualExclusion interface","IMFASFMutualExclusion interface [Media Foundation]","GetStreamsForRecord method","IMFASFMutualExclusion.GetStreamsForRecord","IMFASFMutualExclusion::GetStreamsForRecord","ce410ae9-d0d0-4617-8178-829ef3c77ce0","mf.imfasfmutualexclusion_getstreamsforrecord","wmcontainer/IMFASFMutualExclusion::GetStreamsForRecord"]
old-location: mf\imfasfmutualexclusion_getstreamsforrecord.htm
tech.root: mf
ms.assetid: ce410ae9-d0d0-4617-8178-829ef3c77ce0
ms.date: 12/05/2018
ms.keywords: GetStreamsForRecord, GetStreamsForRecord method [Media Foundation], GetStreamsForRecord method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],GetStreamsForRecord method, IMFASFMutualExclusion.GetStreamsForRecord, IMFASFMutualExclusion::GetStreamsForRecord, ce410ae9-d0d0-4617-8178-829ef3c77ce0, mf.imfasfmutualexclusion_getstreamsforrecord, wmcontainer/IMFASFMutualExclusion::GetStreamsForRecord
req.header: wmcontainer.h
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
 - IMFASFMutualExclusion::GetStreamsForRecord
 - wmcontainer/IMFASFMutualExclusion::GetStreamsForRecord
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
 - IMFASFMutualExclusion.GetStreamsForRecord
---

# IMFASFMutualExclusion::GetStreamsForRecord


## -description

Retrieves the stream numbers contained in a record in the Advanced Systems Format mutual exclusion object.

## -parameters

### -param dwRecordNumber [in]

The number of the record for which to retrieve the stream numbers.

### -param pwStreamNumArray [out]

An array that receives the stream numbers. Set to <b>NULL</b> to get the number of elements required, which is indicated by the value of <i>pcStreams</i> on return. If this parameter is not <b>NULL</b>, the method will copy as many stream numbers to the array as there are elements indicated by the value of <i>pcStreams</i>.

### -param pcStreams [in, out]

On input, the number of elements in the array referenced by <i>pwStreamNumArray</i>. On output, the method sets this value to the count of stream numbers in the record. You can call <b>GetStreamsForRecord</b> with <i>pwStreamNumArray</i> set to <b>NULL</b> to retrieve the number of elements required to hold all of the stream numbers.

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

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>