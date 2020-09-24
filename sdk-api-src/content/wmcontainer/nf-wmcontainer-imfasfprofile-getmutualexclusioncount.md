---
UID: NF:wmcontainer.IMFASFProfile.GetMutualExclusionCount
title: IMFASFProfile::GetMutualExclusionCount (wmcontainer.h)
description: Retrieves the number of Advanced Systems Format (ASF) mutual exclusion objects that are associated with the profile.
helpviewer_keywords: ["5e275b83-9e59-4730-b8e2-e45f78077891","GetMutualExclusionCount","GetMutualExclusionCount method [Media Foundation]","GetMutualExclusionCount method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","GetMutualExclusionCount method","IMFASFProfile.GetMutualExclusionCount","IMFASFProfile::GetMutualExclusionCount","mf.imfasfprofile_getmutualexclusioncount","wmcontainer/IMFASFProfile::GetMutualExclusionCount"]
old-location: mf\imfasfprofile_getmutualexclusioncount.htm
tech.root: mf
ms.assetid: 5e275b83-9e59-4730-b8e2-e45f78077891
ms.date: 12/05/2018
ms.keywords: 5e275b83-9e59-4730-b8e2-e45f78077891, GetMutualExclusionCount, GetMutualExclusionCount method [Media Foundation], GetMutualExclusionCount method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetMutualExclusionCount method, IMFASFProfile.GetMutualExclusionCount, IMFASFProfile::GetMutualExclusionCount, mf.imfasfprofile_getmutualexclusioncount, wmcontainer/IMFASFProfile::GetMutualExclusionCount
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
 - IMFASFProfile::GetMutualExclusionCount
 - wmcontainer/IMFASFProfile::GetMutualExclusionCount
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
 - IMFASFProfile.GetMutualExclusionCount
---

# IMFASFProfile::GetMutualExclusionCount


## -description

Retrieves the number of Advanced Systems Format (ASF) mutual exclusion objects that are associated with the profile.

## -parameters

### -param pcMutexs [out]

Receives the number of mutual exclusion objects.

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

Multiple mutual exclusion objects may be required for streams that are mutually exclusive in more than one way. For more information, see <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord">IMFASFMutualExclusion::AddRecord</a>.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion">IMFASFProfile::GetMutualExclusion</a>