---
UID: NF:wmsdkidl.IWMMetadataEditor2.OpenEx
title: IWMMetadataEditor2::OpenEx (wmsdkidl.h)
description: The OpenEx method opens a file for use by the metadata editor object. OpenEx opens ASF files and MP3 files, though the metadata editor has limited capabilities when working with MP3 files.
helpviewer_keywords: ["IWMMetadataEditor2 interface [windows Media Format]","OpenEx method","IWMMetadataEditor2.OpenEx","IWMMetadataEditor2::OpenEx","IWMMetadataEditor2OpenEx","OpenEx","OpenEx method [windows Media Format]","OpenEx method [windows Media Format]","IWMMetadataEditor2 interface","wmformat.iwmmetadataeditor2_openex","wmsdkidl/IWMMetadataEditor2::OpenEx"]
old-location: wmformat\iwmmetadataeditor2_openex.htm
tech.root: wmformat
ms.assetid: e35f5f85-659e-4a1f-8bfd-4ad3e946d733
ms.date: 4/26/2023
ms.keywords: IWMMetadataEditor2 interface [windows Media Format],OpenEx method, IWMMetadataEditor2.OpenEx, IWMMetadataEditor2::OpenEx, IWMMetadataEditor2OpenEx, OpenEx, OpenEx method [windows Media Format], OpenEx method [windows Media Format],IWMMetadataEditor2 interface, wmformat.iwmmetadataeditor2_openex, wmsdkidl/IWMMetadataEditor2::OpenEx
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMMetadataEditor2::OpenEx
 - wmsdkidl/IWMMetadataEditor2::OpenEx
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
 - IWMMetadataEditor2.OpenEx
---

# IWMMetadataEditor2::OpenEx


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OpenEx</b> method opens a file for use by the metadata editor object. <b>OpenEx</b> opens ASF files and MP3 files, though the metadata editor has limited capabilities when working with MP3 files.

## -parameters

### -param pwszFilename [in]

Pointer to a wide-character null-terminated string containing the file name.

### -param dwDesiredAccess [in]

<b>DWORD</b> containing the desired access type. This can be set to GENERIC_READ or GENERIC_WRITE. For read/write access, pass both values combined with a bitwise <b>OR</b>. When using GENERIC_READ, you must also pass a valid sharing mode as <i>dwShareMode</i>. Failure to do so will result in an error.

### -param dwShareMode [in]

<b>DWORD</b> containing the sharing mode. This can be one of the values in the following table or a combination of the two using a bitwise <b>OR</b>. A value of zero indicates no sharing. Sharing is not supported when requesting read/write access. If you request read/write access and pass any value other than zero for the share mode, an error is returned.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>FILE_SHARE_READ</td>
<td>Subsequent open operations on the file will succeed only if read access is requested.</td>
</tr>
<tr>
<td>FILE_SHARE_DELETE</td>
<td>(NTFS only) Subsequent open operations on the file will succeed only if it is being deleted.</td>
</tr>
</table>

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Read/write access has been requested using file sharing.

OR

Read access has been requested without indicating read-and-delete file sharing.

OR

The access mode requested is not available with this method.

</td>
</tr>
</table>

## -remarks

The parameters <i>dwDesiredAccess</i> and <i>dwShareMode</i> are identical to those used in the <b>OpenFile</b> function defined in the Platform SDK. In the case of <b>OpenEx</b>, however, only a limited set of values are valid for <i>dwDesiredAccess</i>. Using any value other than those specified will result in an error.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2">IWMMetadataEditor2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-open">IWMMetadataEditor::Open</a>