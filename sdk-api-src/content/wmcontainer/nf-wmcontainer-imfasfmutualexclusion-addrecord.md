---
UID: NF:wmcontainer.IMFASFMutualExclusion.AddRecord
title: IMFASFMutualExclusion::AddRecord (wmcontainer.h)
description: Adds a record to the mutual exclusion object. A record specifies streams that are mutually exclusive with the streams in all other records.
helpviewer_keywords: ["AddRecord","AddRecord method [Media Foundation]","AddRecord method [Media Foundation]","IMFASFMutualExclusion interface","IMFASFMutualExclusion interface [Media Foundation]","AddRecord method","IMFASFMutualExclusion.AddRecord","IMFASFMutualExclusion::AddRecord","f5dedc87-a29c-4c8d-b493-486d975f9ac4","mf.imfasfmutualexclusion_addrecord","wmcontainer/IMFASFMutualExclusion::AddRecord"]
old-location: mf\imfasfmutualexclusion_addrecord.htm
tech.root: mf
ms.assetid: f5dedc87-a29c-4c8d-b493-486d975f9ac4
ms.date: 12/05/2018
ms.keywords: AddRecord, AddRecord method [Media Foundation], AddRecord method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],AddRecord method, IMFASFMutualExclusion.AddRecord, IMFASFMutualExclusion::AddRecord, f5dedc87-a29c-4c8d-b493-486d975f9ac4, mf.imfasfmutualexclusion_addrecord, wmcontainer/IMFASFMutualExclusion::AddRecord
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
 - IMFASFMutualExclusion::AddRecord
 - wmcontainer/IMFASFMutualExclusion::AddRecord
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
 - IMFASFMutualExclusion.AddRecord
---

# IMFASFMutualExclusion::AddRecord


## -description

Adds a record to the mutual exclusion object. A record specifies streams that are mutually exclusive with the streams in all other records.

## -parameters

### -param pdwRecordNumber [out]

Receives the index assigned to the new record. Record indexes are zero-based and sequential.

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

A record can include one or more stream numbers. All of the streams in a record are mutually exclusive with all the streams in all other records in the ASF mutual exclusion object.

You can use records to create complex mutual exclusion scenarios by using multiple ASF mutual exclusion objects.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord">IMFASFMutualExclusion::RemoveRecord</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>