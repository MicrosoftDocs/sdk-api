---
UID: NF:wmcontainer.IMFASFMutualExclusion.AddStreamForRecord
title: IMFASFMutualExclusion::AddStreamForRecord (wmcontainer.h)
description: Adds a stream number to a record in the Advanced Systems Format mutual exclusion object.
helpviewer_keywords: ["AddStreamForRecord","AddStreamForRecord method [Media Foundation]","AddStreamForRecord method [Media Foundation]","IMFASFMutualExclusion interface","IMFASFMutualExclusion interface [Media Foundation]","AddStreamForRecord method","IMFASFMutualExclusion.AddStreamForRecord","IMFASFMutualExclusion::AddStreamForRecord","cfbfe3be-b0a4-408a-952e-e4f996f94cee","mf.imfasfmutualexclusion_addstreamforrecord","wmcontainer/IMFASFMutualExclusion::AddStreamForRecord"]
old-location: mf\imfasfmutualexclusion_addstreamforrecord.htm
tech.root: mf
ms.assetid: cfbfe3be-b0a4-408a-952e-e4f996f94cee
ms.date: 12/05/2018
ms.keywords: AddStreamForRecord, AddStreamForRecord method [Media Foundation], AddStreamForRecord method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],AddStreamForRecord method, IMFASFMutualExclusion.AddStreamForRecord, IMFASFMutualExclusion::AddStreamForRecord, cfbfe3be-b0a4-408a-952e-e4f996f94cee, mf.imfasfmutualexclusion_addstreamforrecord, wmcontainer/IMFASFMutualExclusion::AddStreamForRecord
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
 - IMFASFMutualExclusion::AddStreamForRecord
 - wmcontainer/IMFASFMutualExclusion::AddStreamForRecord
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
 - IMFASFMutualExclusion.AddStreamForRecord
---

# IMFASFMutualExclusion::AddStreamForRecord


## -description

Adds a stream number to a record in the Advanced Systems Format mutual exclusion object.

## -parameters

### -param dwRecordNumber [in]

The record number to which the stream is added. A record number is set by the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord">IMFASFMutualExclusion::AddRecord</a> method.

### -param wStreamNumber [in]

The stream number to add to the record.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The specified stream number is already associated with the record.

</td>
</tr>
</table>

## -remarks

Each record includes one or more streams. Every stream in a record is mutually exclusive of all streams in every other record.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord">IMFASFMutualExclusion::GetStreamsForRecord</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord">IMFASFMutualExclusion::RemoveStreamFromRecord</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>