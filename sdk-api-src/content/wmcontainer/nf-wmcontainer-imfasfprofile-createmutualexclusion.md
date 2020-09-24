---
UID: NF:wmcontainer.IMFASFProfile.CreateMutualExclusion
title: IMFASFProfile::CreateMutualExclusion (wmcontainer.h)
description: Creates a new Advanced Systems Format (ASF) mutual exclusion object. Mutual exclusion objects can be added to a profile by calling the AddMutualExclusion method.
helpviewer_keywords: ["457b7b73-34c0-48fe-882a-9cdc3516e20d","CreateMutualExclusion","CreateMutualExclusion method [Media Foundation]","CreateMutualExclusion method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","CreateMutualExclusion method","IMFASFProfile.CreateMutualExclusion","IMFASFProfile::CreateMutualExclusion","mf.imfasfprofile_createmutualexclusion","wmcontainer/IMFASFProfile::CreateMutualExclusion"]
old-location: mf\imfasfprofile_createmutualexclusion.htm
tech.root: mf
ms.assetid: 457b7b73-34c0-48fe-882a-9cdc3516e20d
ms.date: 12/05/2018
ms.keywords: 457b7b73-34c0-48fe-882a-9cdc3516e20d, CreateMutualExclusion, CreateMutualExclusion method [Media Foundation], CreateMutualExclusion method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],CreateMutualExclusion method, IMFASFProfile.CreateMutualExclusion, IMFASFProfile::CreateMutualExclusion, mf.imfasfprofile_createmutualexclusion, wmcontainer/IMFASFProfile::CreateMutualExclusion
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
 - IMFASFProfile::CreateMutualExclusion
 - wmcontainer/IMFASFProfile::CreateMutualExclusion
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
 - IMFASFProfile.CreateMutualExclusion
---

# IMFASFProfile::CreateMutualExclusion


## -description

Creates a new Advanced Systems Format (ASF) mutual exclusion object. Mutual exclusion objects can be added to a profile by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion">AddMutualExclusion</a> method.

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

The ASF mutual exclusion object created by this method is not associated with the profile. Call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion">IMFASFProfile::AddMutualExclusion</a> after configuring the object to make this association.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>