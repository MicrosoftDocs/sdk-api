---
UID: NF:wmcontainer.IMFASFProfile.GetMutualExclusion
title: IMFASFProfile::GetMutualExclusion (wmcontainer.h)
description: Retrieves an Advanced Systems Format (ASF) mutual exclusion object from the profile.
helpviewer_keywords: ["9b9e37fc-0bd8-4502-9e90-76330a08f68b","GetMutualExclusion","GetMutualExclusion method [Media Foundation]","GetMutualExclusion method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","GetMutualExclusion method","IMFASFProfile.GetMutualExclusion","IMFASFProfile::GetMutualExclusion","mf.imfasfprofile_getmutualexclusion","wmcontainer/IMFASFProfile::GetMutualExclusion"]
old-location: mf\imfasfprofile_getmutualexclusion.htm
tech.root: mf
ms.assetid: 9b9e37fc-0bd8-4502-9e90-76330a08f68b
ms.date: 12/05/2018
ms.keywords: 9b9e37fc-0bd8-4502-9e90-76330a08f68b, GetMutualExclusion, GetMutualExclusion method [Media Foundation], GetMutualExclusion method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetMutualExclusion method, IMFASFProfile.GetMutualExclusion, IMFASFProfile::GetMutualExclusion, mf.imfasfprofile_getmutualexclusion, wmcontainer/IMFASFProfile::GetMutualExclusion
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
 - IMFASFProfile::GetMutualExclusion
 - wmcontainer/IMFASFProfile::GetMutualExclusion
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
 - IMFASFProfile.GetMutualExclusion
---

# IMFASFProfile::GetMutualExclusion


## -description

Retrieves an Advanced Systems Format (ASF) mutual exclusion object from the profile.

## -parameters

### -param dwMutexIndex [in]

Index of the mutual exclusion object in the profile.

### -param ppIMutex [out]

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a> interface of the ASF mutual exclusion object. The caller must release the interface.

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

This method does not create a copy of the mutual exclusion object. The returned pointer refers to the mutual exclusion contained in the profile object. You must not make any changes to the mutual exclusion object using this pointer, because doing so can affect the profile object in unexpected ways.

To change the configuration of the mutual exclusion object in the profile, you must first clone the mutual exclusion object by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone">IMFASFMutualExclusion::Clone</a>. Make whatever changes are required to the clone of the object, remove the old mutual exclusion object from the profile by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion">IMFASFProfile::RemoveMutualExclusion</a> method, and then add the updated object by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion">IMFASFProfile::AddMutualExclusion</a> method.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion">IMFASFProfile::AddMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount">IMFASFProfile::GetMutualExclusionCount</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion">IMFASFProfile::RemoveMutualExclusion</a>