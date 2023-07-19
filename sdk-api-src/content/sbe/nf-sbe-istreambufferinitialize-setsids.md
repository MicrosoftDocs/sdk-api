---
UID: NF:sbe.IStreamBufferInitialize.SetSIDs
title: IStreamBufferInitialize::SetSIDs (sbe.h)
description: The SetSIDs method sets the security identifiers (SIDs) that are used to protect access to the backing files.
helpviewer_keywords: ["IStreamBufferInitialize interface [Microsoft TV Technologies]","SetSIDs method","IStreamBufferInitialize.SetSIDs","IStreamBufferInitialize::SetSIDs","IStreamBufferInitializeSetSIDs","SetSIDs","SetSIDs method [Microsoft TV Technologies]","SetSIDs method [Microsoft TV Technologies]","IStreamBufferInitialize interface","mstv.istreambufferinitialize_setsids","sbe/IStreamBufferInitialize::SetSIDs"]
old-location: mstv\istreambufferinitialize_setsids.htm
tech.root: mstv
ms.assetid: bd25a967-9335-4bbd-ac85-f8b25f2be563
ms.date: 12/05/2018
ms.keywords: IStreamBufferInitialize interface [Microsoft TV Technologies],SetSIDs method, IStreamBufferInitialize.SetSIDs, IStreamBufferInitialize::SetSIDs, IStreamBufferInitializeSetSIDs, SetSIDs, SetSIDs method [Microsoft TV Technologies], SetSIDs method [Microsoft TV Technologies],IStreamBufferInitialize interface, mstv.istreambufferinitialize_setsids, sbe/IStreamBufferInitialize::SetSIDs
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
 - IStreamBufferInitialize::SetSIDs
 - sbe/IStreamBufferInitialize::SetSIDs
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
 - IStreamBufferInitialize.SetSIDs
---

# IStreamBufferInitialize::SetSIDs


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetSIDs</b> method sets the security identifiers (SIDs) that are used to protect access to the backing files.

## -parameters

### -param cSIDs [in]

Specifies the size of the array given in the <i>ppSID</i> parameter.

### -param ppSID [in]

Pointer to an array of <b>SID</b> structures, of size <i>cSIDs</i>.

## -returns

Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

</td>
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

At run time, the Stream Buffer Source and Sink filters create various Win32 objects, such as mutexes, so that access to the backing files is synchronized across threads. Each of the filters maintains a list of SIDs that are used to protect these objects. By default, the filters inherit their SIDs from the hosting process. An application can use the <b>SetSIDs</b> method to override the default SIDs.

If you call this method, do so before locking the sink filter or loading a file in the source filter. It is recommended that all of the filters be given the same SIDs.

<ul>
<li>
<div class="alert"><b>Important</b>  Setting less-privileged SIDs can create a security issue.</div>
<div> </div>
</li>
</ul>
Note that this method does not apply to content recording files, which are protected by the discretionary access-control lists (DACLs) of the directory structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferinitialize">IStreamBufferInitialize Interface</a>