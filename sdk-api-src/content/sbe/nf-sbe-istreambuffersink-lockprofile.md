---
UID: NF:sbe.IStreamBufferSink.LockProfile
title: IStreamBufferSink::LockProfile (sbe.h)
description: The LockProfile method locks the Stream Buffer Sink filter's profile, thereby fixing the number of streams and their media types. This method can also specify the name and location of the stub file that points to the backing files.
helpviewer_keywords: ["IStreamBufferSink interface [Microsoft TV Technologies]","LockProfile method","IStreamBufferSink.LockProfile","IStreamBufferSink::LockProfile","IStreamBufferSinkLockProfile","LockProfile","LockProfile method [Microsoft TV Technologies]","LockProfile method [Microsoft TV Technologies]","IStreamBufferSink interface","mstv.istreambuffersink_lockprofile","sbe/IStreamBufferSink::LockProfile"]
old-location: mstv\istreambuffersink_lockprofile.htm
tech.root: mstv
ms.assetid: 9e694cc2-090e-43b1-88c7-77175a930bf1
ms.date: 12/05/2018
ms.keywords: IStreamBufferSink interface [Microsoft TV Technologies],LockProfile method, IStreamBufferSink.LockProfile, IStreamBufferSink::LockProfile, IStreamBufferSinkLockProfile, LockProfile, LockProfile method [Microsoft TV Technologies], LockProfile method [Microsoft TV Technologies],IStreamBufferSink interface, mstv.istreambuffersink_lockprofile, sbe/IStreamBufferSink::LockProfile
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
 - IStreamBufferSink::LockProfile
 - sbe/IStreamBufferSink::LockProfile
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
 - IStreamBufferSink.LockProfile
---

# IStreamBufferSink::LockProfile


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>LockProfile</b> method locks the Stream Buffer Sink filter's profile, thereby fixing the number of streams and their media types. This method can also specify the name and location of the stub file that points to the backing files.

## -parameters

### -param pszStreamBufferFilename [in]

Pointer to a null-terminated wide-character string that specifies the full path name of the stub file. If the specified file already exists, the method fails. If <i>pszFilename</i> is <b>NULL</b>, the stub file is created in the current directory with a default file name.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded. (Multiple calls with the same parameter.)

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_UNSUPPORTED_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The call failed because there are no streams in the profile.

</td>
</tr>
</table>

## -remarks

The profile describes the number of input streams, their media types, and the location of the stub file that points to the temporary backing files. The profile must be locked before the Stream Buffer Source filter can read data from the backing files. Applications can lock the profile explicitly by calling the <b>LockProfile</b> method, or implicitly by running the filter graph that contains the Stream Buffer Sink filter.

After the profile is locked, the Stream Buffer Sink filter does not accept any new pin connections. Pins already connected can be reconnected, but only with the same media type. The profile is unlocked when the graph stops.

The stub file is automatically deleted when the last process closes the file handle. This occurs when the capture graph stops and no render graphs are reading the file.

After the first successful call to this method, further calls with the same value of <i>pszFileName</i> return S_FALSE. Further calls with a different value for <i>pszFileName</i> fail and return E_UNEXPECTED.

The name of the stub file can be given to the Stream Buffer Source filter through that filter's <a href="/windows/desktop/api/strmif/nf-strmif-ifilesourcefilter-load">IFileSourceFilter::Load</a> method.

<h3><a id="Windows_Vista_or_later"></a><a id="windows_vista_or_later"></a><a id="WINDOWS_VISTA_OR_LATER"></a>Windows Vista or later</h3>
This method requires administrator privileges, unless you first call <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure3-setnamespace">IStreamBufferConfigure3::SetNamespace</a> with the value <b>NULL</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersink">IStreamBufferSink Interface</a>