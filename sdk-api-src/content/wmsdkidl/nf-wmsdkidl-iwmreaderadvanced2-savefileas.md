---
UID: NF:wmsdkidl.IWMReaderAdvanced2.SaveFileAs
title: IWMReaderAdvanced2::SaveFileAs (wmsdkidl.h)
description: The SaveFileAs method saves the current file.
helpviewer_keywords: ["IWMReaderAdvanced2 interface [windows Media Format]","SaveFileAs method","IWMReaderAdvanced2.SaveFileAs","IWMReaderAdvanced2::SaveFileAs","IWMReaderAdvanced2SaveFileAs","SaveFileAs","SaveFileAs method [windows Media Format]","SaveFileAs method [windows Media Format]","IWMReaderAdvanced2 interface","wmformat.iwmreaderadvanced2_savefileas","wmsdkidl/IWMReaderAdvanced2::SaveFileAs"]
old-location: wmformat\iwmreaderadvanced2_savefileas.htm
tech.root: wmformat
ms.assetid: 97bdac1f-8830-45c0-9229-322ad72b3954
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],SaveFileAs method, IWMReaderAdvanced2.SaveFileAs, IWMReaderAdvanced2::SaveFileAs, IWMReaderAdvanced2SaveFileAs, SaveFileAs, SaveFileAs method [windows Media Format], SaveFileAs method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_savefileas, wmsdkidl/IWMReaderAdvanced2::SaveFileAs
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
 - IWMReaderAdvanced2::SaveFileAs
 - wmsdkidl/IWMReaderAdvanced2::SaveFileAs
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
 - IWMReaderAdvanced2.SaveFileAs
---

# IWMReaderAdvanced2::SaveFileAs


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SaveFileAs</b> method saves the current file.

## -parameters

### -param pwszFilename [in]

Pointer to a wide-character null-terminated string containing the file name.

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
<dt><b>ERROR_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The file was closed before the operation completed. A WMT_SAVEAS_STOP event is also generated in this case.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The call to this method has been made before an <b>Open</b> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
A previous <b>SaveFileAs</b> operation has not yet been completed. Saving files is sequential.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The play mode is not WMT_PLAY_MODE_DOWNLOAD.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
There is not enough free disk space. See the note in the Remarks below.

</td>
</tr>
</table>

## -remarks

This method can be used to save the content downloaded from a Web server to the local hard disk. Files can be saved when the reader is downloading from a Web server.

You can use this method to save a server-side playlist. When you do so, you specify the name to use for the playlist, and each file in the playlist will be saved automatically.

This operation is asynchronous; WMT_SAVEAS_STOP indicates that all the data has been saved. Closing the reader ends a save operation that has not been completed.

This method can take some time to complete, and a call can be made to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getsaveasprogress">GetSaveAsProgress</a> to determine progress.

<div class="alert"><b>Note</b>  It is possible to get the out of disk space error (STG_E_MEDIUMFULL) if the file being saved is greater than 1 MB. This is because Microsoft Internet Explorer has a maximum cache size of 1MB, and in this case the error does not refer to the amount of free disk space. This effectively limits the sizes of files that can be saved this way to those under 1 MB.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>