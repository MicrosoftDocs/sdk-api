---
UID: NF:sbe.IStreamBufferRecComp.Initialize
title: IStreamBufferRecComp::Initialize (sbe.h)
description: The Initialize method sets the file name and the profile for the new recording. Call this method once, after creating the RecComp object.
helpviewer_keywords: ["IStreamBufferRecComp interface [Microsoft TV Technologies]","Initialize method","IStreamBufferRecComp.Initialize","IStreamBufferRecComp::Initialize","IStreamBufferRecCompInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IStreamBufferRecComp interface","mstv.istreambufferreccomp_initialize","sbe/IStreamBufferRecComp::Initialize"]
old-location: mstv\istreambufferreccomp_initialize.htm
tech.root: mstv
ms.assetid: 97a8519f-2377-43e9-b1ba-7d407caa44a9
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecComp interface [Microsoft TV Technologies],Initialize method, IStreamBufferRecComp.Initialize, IStreamBufferRecComp::Initialize, IStreamBufferRecCompInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IStreamBufferRecComp interface, mstv.istreambufferreccomp_initialize, sbe/IStreamBufferRecComp::Initialize
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferRecComp::Initialize
 - sbe/IStreamBufferRecComp::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecComp.Initialize
---

# IStreamBufferRecComp::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Initialize</b> method sets the file name and the profile for the new recording. Call this method once, after creating the <a href="/previous-versions/windows/desktop/mstv/reccomp-object">RecComp</a> object.

## -parameters

### -param pszTargetFilename [in]

Null-terminated, wide character string that specifies the file name of the new recording.

### -param pszSBRecProfileRef [in]

Null-terminated, wide character string that specifies an existing file. This file must be a complete recording, already created by the Stream Buffer Engine.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
Success

</td>
</tr>
</table>

## -remarks

The profile of the file specified by <i>pszSBRecProfileRef</i> will be used for the target file. All files that are appended to the target file must have the same profile. For more information about profiles, see <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-lockprofile">IStreamBufferSink::LockProfile</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferreccomp">IStreamBufferRecComp Interface</a>