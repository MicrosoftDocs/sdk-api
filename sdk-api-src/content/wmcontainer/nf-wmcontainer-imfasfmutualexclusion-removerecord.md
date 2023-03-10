---
UID: NF:wmcontainer.IMFASFMutualExclusion.RemoveRecord
title: IMFASFMutualExclusion::RemoveRecord (wmcontainer.h)
description: Removes a record from the Advanced Systems Format (ASF) mutual exclusion object.
helpviewer_keywords: ["IMFASFMutualExclusion interface [Media Foundation]","RemoveRecord method","IMFASFMutualExclusion.RemoveRecord","IMFASFMutualExclusion::RemoveRecord","RemoveRecord","RemoveRecord method [Media Foundation]","RemoveRecord method [Media Foundation]","IMFASFMutualExclusion interface","ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8","mf.imfasfmutualexclusion_removerecord","wmcontainer/IMFASFMutualExclusion::RemoveRecord"]
old-location: mf\imfasfmutualexclusion_removerecord.htm
tech.root: mf
ms.assetid: ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8
ms.date: 12/05/2018
ms.keywords: IMFASFMutualExclusion interface [Media Foundation],RemoveRecord method, IMFASFMutualExclusion.RemoveRecord, IMFASFMutualExclusion::RemoveRecord, RemoveRecord, RemoveRecord method [Media Foundation], RemoveRecord method [Media Foundation],IMFASFMutualExclusion interface, ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8, mf.imfasfmutualexclusion_removerecord, wmcontainer/IMFASFMutualExclusion::RemoveRecord
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
 - IMFASFMutualExclusion::RemoveRecord
 - wmcontainer/IMFASFMutualExclusion::RemoveRecord
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
 - IMFASFMutualExclusion.RemoveRecord
---

# IMFASFMutualExclusion::RemoveRecord


## -description

Removes a record from the Advanced Systems Format (ASF) mutual exclusion object.

## -parameters

### -param dwRecordNumber [in]

The index of the record to remove.

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

When a record is removed, the ASF mutual exclusion object indexes the remaining records so that they are sequential starting with zero. You should enumerate the records to ensure that you have the correct index for each record. If the record removed is the one with the highest index, removing it has no effect on the other indexes.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord">IMFASFMutualExclusion::AddRecord</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>