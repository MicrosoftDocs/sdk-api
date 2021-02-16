---
UID: NF:wmcontainer.IMFASFMutualExclusion.GetRecordCount
title: IMFASFMutualExclusion::GetRecordCount (wmcontainer.h)
description: Retrieves the number of records in the Advanced Systems Format mutual exclusion object.
helpviewer_keywords: ["8dbd883e-4ae3-422d-bb2e-087a9e311558","GetRecordCount","GetRecordCount method [Media Foundation]","GetRecordCount method [Media Foundation]","IMFASFMutualExclusion interface","IMFASFMutualExclusion interface [Media Foundation]","GetRecordCount method","IMFASFMutualExclusion.GetRecordCount","IMFASFMutualExclusion::GetRecordCount","mf.imfasfmutualexclusion_getrecordcount","wmcontainer/IMFASFMutualExclusion::GetRecordCount"]
old-location: mf\imfasfmutualexclusion_getrecordcount.htm
tech.root: mf
ms.assetid: 8dbd883e-4ae3-422d-bb2e-087a9e311558
ms.date: 12/05/2018
ms.keywords: 8dbd883e-4ae3-422d-bb2e-087a9e311558, GetRecordCount, GetRecordCount method [Media Foundation], GetRecordCount method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],GetRecordCount method, IMFASFMutualExclusion.GetRecordCount, IMFASFMutualExclusion::GetRecordCount, mf.imfasfmutualexclusion_getrecordcount, wmcontainer/IMFASFMutualExclusion::GetRecordCount
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
 - IMFASFMutualExclusion::GetRecordCount
 - wmcontainer/IMFASFMutualExclusion::GetRecordCount
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
 - IMFASFMutualExclusion.GetRecordCount
---

# IMFASFMutualExclusion::GetRecordCount


## -description

Retrieves the number of records in the Advanced Systems Format mutual exclusion object.

## -parameters

### -param pdwRecordCount [out]

Receives the count of records.

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

Each record includes one or more streams. Every stream in a record is mutually exclusive of streams in every other record.

Use this method in conjunction with <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord">IMFASFMutualExclusion::GetStreamsForRecord</a> to retrieve the streams that are included in each record.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord">IMFASFMutualExclusion::AddRecord</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord">IMFASFMutualExclusion::GetStreamsForRecord</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord">IMFASFMutualExclusion::RemoveRecord</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>