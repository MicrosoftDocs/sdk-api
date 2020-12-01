---
UID: NF:wmcontainer.IMFASFProfile.AddMutualExclusion
title: IMFASFProfile::AddMutualExclusion (wmcontainer.h)
description: Adds a configured Advanced Systems Format (ASF) mutual exclusion object to the profile.
helpviewer_keywords: ["AddMutualExclusion","AddMutualExclusion method [Media Foundation]","AddMutualExclusion method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","AddMutualExclusion method","IMFASFProfile.AddMutualExclusion","IMFASFProfile::AddMutualExclusion","d9069feb-7d39-4b40-b95e-0112d959bbae","mf.imfasfprofile_addmutualexclusion","wmcontainer/IMFASFProfile::AddMutualExclusion"]
old-location: mf\imfasfprofile_addmutualexclusion.htm
tech.root: mf
ms.assetid: d9069feb-7d39-4b40-b95e-0112d959bbae
ms.date: 12/05/2018
ms.keywords: AddMutualExclusion, AddMutualExclusion method [Media Foundation], AddMutualExclusion method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],AddMutualExclusion method, IMFASFProfile.AddMutualExclusion, IMFASFProfile::AddMutualExclusion, d9069feb-7d39-4b40-b95e-0112d959bbae, mf.imfasfprofile_addmutualexclusion, wmcontainer/IMFASFProfile::AddMutualExclusion
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
 - IMFASFProfile::AddMutualExclusion
 - wmcontainer/IMFASFProfile::AddMutualExclusion
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
 - IMFASFProfile.AddMutualExclusion
---

# IMFASFProfile::AddMutualExclusion


## -description

Adds a configured Advanced Systems Format (ASF) mutual exclusion object to the profile.

## -parameters

### -param pIMutex [in]

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a> interface of a configured ASF mutual exclusion object.

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

You can create a mutual exclusion object by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion">IMFASFProfile::CreateMutualExclusion</a> method.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion">IMFASFProfile::GetMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion">IMFASFProfile::RemoveMutualExclusion</a>