---
UID: NF:wmcontainer.IMFASFMutualExclusion.Clone
title: IMFASFMutualExclusion::Clone (wmcontainer.h)
description: Creates a copy of the Advanced Systems Format mutual exclusion object.
helpviewer_keywords: ["32bd09d7-9d85-4692-8b2f-6afab3234fa9","Clone","Clone method [Media Foundation]","Clone method [Media Foundation]","IMFASFMutualExclusion interface","IMFASFMutualExclusion interface [Media Foundation]","Clone method","IMFASFMutualExclusion.Clone","IMFASFMutualExclusion::Clone","mf.imfasfmutualexclusion_clone","wmcontainer/IMFASFMutualExclusion::Clone"]
old-location: mf\imfasfmutualexclusion_clone.htm
tech.root: mf
ms.assetid: 32bd09d7-9d85-4692-8b2f-6afab3234fa9
ms.date: 12/05/2018
ms.keywords: 32bd09d7-9d85-4692-8b2f-6afab3234fa9, Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],Clone method, IMFASFMutualExclusion.Clone, IMFASFMutualExclusion::Clone, mf.imfasfmutualexclusion_clone, wmcontainer/IMFASFMutualExclusion::Clone
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
 - IMFASFMutualExclusion::Clone
 - wmcontainer/IMFASFMutualExclusion::Clone
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
 - IMFASFMutualExclusion.Clone
---

# IMFASFMutualExclusion::Clone


## -description

Creates a copy of the Advanced Systems Format mutual exclusion object.

## -parameters

### -param ppIMutex [out]

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a> interface of the new object. The caller must release the interface.

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

The cloned object is a new object, completely independent of the object from which it was cloned.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>