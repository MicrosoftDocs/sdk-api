---
UID: NF:wmcontainer.IMFASFMutualExclusion.SetType
title: IMFASFMutualExclusion::SetType (wmcontainer.h)
description: Sets the type of mutual exclusion that is represented by the Advanced Systems Format (ASF) mutual exclusion object.
helpviewer_keywords: ["58fc1c27-0a7d-48bb-b5a4-ab299c5e0ac6","IMFASFMutualExclusion interface [Media Foundation]","SetType method","IMFASFMutualExclusion.SetType","IMFASFMutualExclusion::SetType","SetType","SetType method [Media Foundation]","SetType method [Media Foundation]","IMFASFMutualExclusion interface","mf.imfasfmutualexclusion_settype","wmcontainer/IMFASFMutualExclusion::SetType"]
old-location: mf\imfasfmutualexclusion_settype.htm
tech.root: mf
ms.assetid: 58fc1c27-0a7d-48bb-b5a4-ab299c5e0ac6
ms.date: 12/05/2018
ms.keywords: 58fc1c27-0a7d-48bb-b5a4-ab299c5e0ac6, IMFASFMutualExclusion interface [Media Foundation],SetType method, IMFASFMutualExclusion.SetType, IMFASFMutualExclusion::SetType, SetType, SetType method [Media Foundation], SetType method [Media Foundation],IMFASFMutualExclusion interface, mf.imfasfmutualexclusion_settype, wmcontainer/IMFASFMutualExclusion::SetType
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
 - IMFASFMutualExclusion::SetType
 - wmcontainer/IMFASFMutualExclusion::SetType
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
 - IMFASFMutualExclusion.SetType
---

# IMFASFMutualExclusion::SetType


## -description

Sets the type of mutual exclusion that is represented by the Advanced Systems Format (ASF) mutual exclusion object.

## -parameters

### -param guidType [in]

The type of mutual exclusion that is represented by the ASF mutual exclusion object. For a list of predefined mutual exclusion type constants, see <a href="/windows/desktop/medfound/asf-mutual-exclusion-type-guids">ASF Mutual Exclusion Type GUIDs</a>.

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

Sometimes, content must be made mutually exclusive in more than one way. For example, a video file might contain audio streams in several bit rates for each of several languages. To handle this type of complex mutual exclusion, you must configure more than one ASF mutual exclusion object. For more information, see <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord">IMFASFMutualExclusion::AddRecord</a>.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion">IMFASFMutualExclusion</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype">IMFASFMutualExclusion::GetType</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>