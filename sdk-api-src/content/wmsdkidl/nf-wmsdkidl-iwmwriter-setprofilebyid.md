---
UID: NF:wmsdkidl.IWMWriter.SetProfileByID
title: IWMWriter::SetProfileByID (wmsdkidl.h)
description: The SetProfileByID method specifies the profile to use for the current writing task, identifying the profile by its GUID.
helpviewer_keywords: ["IWMWriter interface [windows Media Format]","SetProfileByID method","IWMWriter.SetProfileByID","IWMWriter::SetProfileByID","IWMWriterSetProfileByID","SetProfileByID","SetProfileByID method [windows Media Format]","SetProfileByID method [windows Media Format]","IWMWriter interface","wmformat.iwmwriter_setprofilebyid","wmsdkidl/IWMWriter::SetProfileByID"]
old-location: wmformat\iwmwriter_setprofilebyid.htm
tech.root: wmformat
ms.assetid: 743212fd-a1e7-47c5-a220-c203cc2788e6
ms.date: 4/26/2023
ms.keywords: IWMWriter interface [windows Media Format],SetProfileByID method, IWMWriter.SetProfileByID, IWMWriter::SetProfileByID, IWMWriterSetProfileByID, SetProfileByID, SetProfileByID method [windows Media Format], SetProfileByID method [windows Media Format],IWMWriter interface, wmformat.iwmwriter_setprofilebyid, wmsdkidl/IWMWriter::SetProfileByID
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriter::SetProfileByID
 - wmsdkidl/IWMWriter::SetProfileByID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriter.SetProfileByID
---

# IWMWriter::SetProfileByID


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetProfileByID</b> method specifies the profile to use for the current writing task, identifying the profile by its GUID.

## -parameters

### -param guidProfile [in]

GUID of the profile.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>

## -remarks

Only system profiles have IDs. Use the methods of the <b>IWMProfileManager</b> interface to examine system profiles. The header file Wmsysprf.h has a list of system profiles and their IDs.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile">IWMWriter::SetProfile</a>



<a href="/windows/desktop/wmformat/to-use-profiles-with-the-writer">To Use Profiles with the Writer</a>