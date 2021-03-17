---
UID: NF:wmcontainer.IMFASFProfile.RemoveMutualExclusion
title: IMFASFProfile::RemoveMutualExclusion (wmcontainer.h)
description: Removes an Advanced Systems Format (ASF) mutual exclusion object from the profile.
helpviewer_keywords: ["IMFASFProfile interface [Media Foundation]","RemoveMutualExclusion method","IMFASFProfile.RemoveMutualExclusion","IMFASFProfile::RemoveMutualExclusion","RemoveMutualExclusion","RemoveMutualExclusion method [Media Foundation]","RemoveMutualExclusion method [Media Foundation]","IMFASFProfile interface","dbcf192f-1ab4-44c4-8444-5d2aba941fe1","mf.imfasfprofile_removemutualexclusion","wmcontainer/IMFASFProfile::RemoveMutualExclusion"]
old-location: mf\imfasfprofile_removemutualexclusion.htm
tech.root: mf
ms.assetid: dbcf192f-1ab4-44c4-8444-5d2aba941fe1
ms.date: 12/05/2018
ms.keywords: IMFASFProfile interface [Media Foundation],RemoveMutualExclusion method, IMFASFProfile.RemoveMutualExclusion, IMFASFProfile::RemoveMutualExclusion, RemoveMutualExclusion, RemoveMutualExclusion method [Media Foundation], RemoveMutualExclusion method [Media Foundation],IMFASFProfile interface, dbcf192f-1ab4-44c4-8444-5d2aba941fe1, mf.imfasfprofile_removemutualexclusion, wmcontainer/IMFASFProfile::RemoveMutualExclusion
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
 - IMFASFProfile::RemoveMutualExclusion
 - wmcontainer/IMFASFProfile::RemoveMutualExclusion
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
 - IMFASFProfile.RemoveMutualExclusion
---

# IMFASFProfile::RemoveMutualExclusion


## -description

Removes an Advanced Systems Format (ASF) mutual exclusion object from the profile.

## -parameters

### -param dwMutexIndex [in]

The index of the mutual exclusion object to remove from the profile.

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

When a mutual exclusion object is removed from the profile, the ASF profile object reassigns the mutual exclusion indexes so that they are sequential starting with zero. Any previously stored indexes are no longer valid after calling this method.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion">IMFASFProfile::AddMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion">IMFASFProfile::GetMutualExclusion</a>