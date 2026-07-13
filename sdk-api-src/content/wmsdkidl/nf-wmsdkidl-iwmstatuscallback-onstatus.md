---
UID: NF:wmsdkidl.IWMStatusCallback.OnStatus
title: IWMStatusCallback::OnStatus (wmsdkidl.h)
description: The OnStatus method is called when status information must be communicated to the application.
helpviewer_keywords: ["IWMStatusCallback interface [windows Media Format]","OnStatus method","IWMStatusCallback.OnStatus","IWMStatusCallback::OnStatus","IWMStatusCallbackOnStatus","OnStatus","OnStatus method [windows Media Format]","OnStatus method [windows Media Format]","IWMStatusCallback interface","wmformat.iwmstatuscallback_onstatus","wmsdkidl/IWMStatusCallback::OnStatus"]
old-location: wmformat\iwmstatuscallback_onstatus.htm
tech.root: wmformat
ms.assetid: 7b8cdb21-96e1-4cf9-8422-72bce693afb1
ms.date: 4/26/2023
ms.keywords: IWMStatusCallback interface [windows Media Format],OnStatus method, IWMStatusCallback.OnStatus, IWMStatusCallback::OnStatus, IWMStatusCallbackOnStatus, OnStatus, OnStatus method [windows Media Format], OnStatus method [windows Media Format],IWMStatusCallback interface, wmformat.iwmstatuscallback_onstatus, wmsdkidl/IWMStatusCallback::OnStatus
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMStatusCallback::OnStatus
 - wmsdkidl/IWMStatusCallback::OnStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMStatusCallback.OnStatus
---

# IWMStatusCallback::OnStatus


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnStatus</b> method is called when status information must be communicated to the application.

## -parameters

### -param Status [in]

One member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status">WMT_STATUS</a> enumeration type. For a description of possible <b>WMT_STATUS</b> values, see the tables in the Remarks section.

### -param hr [in]

<b>HRESULT</b> error code. If this indicates failure, you should not process the status as normal, as some error has occurred. Use <code>if (FAILED(hr))</code> to check for a failed value. See the topic <a href="/windows/desktop/wmformat/error-codes">Error Codes</a> for a list of possible results.

### -param dwType [in]

Member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. This value specifies the type of data in the buffer at <i>pValue</i>.

### -param pValue [in]

Pointer to a byte array containing the value. The contents of this array depend on the value of <i>Status</i> and the value of <i>dwType</i>.

### -param pvContext [in]

Generic pointer provided by the application, for its own use. This pointer matches the context pointer given to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>, <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing">IWMIndexer::StartIndexing</a>, and other methods. The SDK makes no assumptions about the use of this pointer; it is simply provided by the application and passed back to the application when a callback is made.

## -returns

This method is implemented by the application. It should always return S_OK.

## -remarks

The contents of <i>pParam</i> depend on those of <i>Status</i>.

The following <b>WMT_STATUS</b> values can be passed to this method by the reader.

<table>
<tr>
<th>Member
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>WMT_ACQUIRE_LICENSE</td>
<td>The license acquisition process is complete. If the license acquisition is unsuccessful, an error is returned in the <i>hr</i> parameter. If the license acquisition is successful, S_OK is returned in the <i>hr</i> parameter, and a <a href="/windows/desktop/wmformat/wm-get-license-data">WM_GET_LICENSE_DATA</a> data structure is returned in the <i>pvalue</i> parameter.</td>
</tr>
<tr>
<td>WMT_BUFFERING_START</td>
<td>The reader has started buffering data.</td>
</tr>
<tr>
<td>WMT_BUFFERING_STOP</td>
<td>The reader has stopped buffering data.</td>
</tr>
<tr>
<td>WMT_CLOSED</td>
<td>The reader has closed the file.</td>
</tr>
<tr>
<td>WMT_CONNECTING</td>
<td>The reader is connecting to a server.</td>
</tr>
<tr>
<td>WMT_END_OF_FILE</td>
<td>The reader has reached the end of the file.</td>
</tr>
<tr>
<td>WMT_END_OF_SEGMENT</td>
<td>When the <b>Start</b> method is called with a duration argument, WMT_END_OF_SEGMENT is returned when playback has been completed after the specified period. The argument is a <b>QWORD</b> indicating duration of playback in 100-nanosecond units.</td>
</tr>
<tr>
<td>WMT_END_OF_STREAMING</td>
<td>The file has finished streaming.</td>
</tr>
<tr>
<td>WMT_EOF</td>
<td>The reader has reached the end of the file.</td>
</tr>
<tr>
<td>WMT_ERROR</td>
<td>An error occurred in reading the file.</td>
</tr>
<tr>
<td>WMT_INDIVIDUALIZE</td>
<td>The individualization process is in progress or has completed. This event is sent repeatedly during the individualization process. <i>pvalue</i> contains a <a href="/windows/desktop/wmformat/wm-individualize-status">WM_INDIVIDUALIZE_STATUS</a> structure that contains status information about the progress of the download.</td>
</tr>
<tr>
<td>WMT_LOCATING</td>
<td>The reader is locating a server.</td>
</tr>
<tr>
<td>WMT_MISSING_CODEC</td>
<td>The reader does not have the appropriate codec to decompress this file.</td>
</tr>
<tr>
<td>WMT_NEEDS_INDIVIDUALIZATION</td>
<td>The client needs a security update.</td>
</tr>
<tr>
<td>WMT_NEW_METADATA</td>
<td>The metadata has changed for the current source.</td>
</tr>
<tr>
<td>WMT_NEW_SOURCEFLAGS</td>
<td>There has been a change to the settings for the current source.</td>
</tr>
<tr>
<td>WMT_NO_RIGHTS</td>
<td>The reader has tried to play back DRM version 1 content and the computer does not have an appropriate license to play it.</td>
</tr>
<tr>
<td>WMT_NO_RIGHTS_EX</td>
<td>The reader has tried to play back DRM version 7 content and the computer does not have an appropriate license to play it.</td>
</tr>
<tr>
<td>WMT_OPENED</td>
<td>The file has been opened for reading.</td>
</tr>
<tr>
<td>WMT_SAVEAS_START</td>
<td>Starting to save the file to disk.</td>
</tr>
<tr>
<td>WMT_SAVEAS_STOP</td>
<td>Stopped saving the file to disk.</td>
</tr>
<tr>
<td>WMT_SOURCE_SWITCH</td>
<td>There has been a change in source file or stream.</td>
</tr>
<tr>
<td>WMT_STARTED</td>
<td>The reader has started reading the file. The <i>pValue</i> parameter points to a <b>QWORD</b> that indicates the starting timestamp. If it is -1 the starting timestamp is 0. When the value is any other negative number, it should be converted to a positive to give the starting timestamp.</td>
</tr>
<tr>
<td>WMT_STOPPED</td>
<td>The reader has stopped reading the file.</td>
</tr>
<tr>
<td>WMT_TIMER</td>
<td>A timer event has occurred.</td>
</tr>
</table>
 

The following <b>WMT_STATUS</b> values can be passed to the callback by the writer file sink.

<table>
<tr>
<th>Member
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>WMT_ERROR</td>
<td>An error occurred in writing the file.</td>
</tr>
<tr>
<td>WMT_OPENED</td>
<td>The file has been opened for writing.</td>
</tr>
<tr>
<td>WMT_STARTED</td>
<td>The writer has started writing the file. The <i>pValue</i> parameter points to a <b>QWORD</b> that indicates the starting timestamp. If it is -1 the starting timestamp is 0. When the value is any other negative number, it should be converted to a positive to give the starting timestamp.</td>
</tr>
<tr>
<td>WMT_STOPPED</td>
<td>The writer has stopped writing the file.</td>
</tr>
<tr>
<td>WMT_CLOSED</td>
<td>The writer has closed the file.</td>
</tr>
</table>
 

The following <b>WMT_STATUS</b> enumeration values can be passed to the callback by the writer network sink.

<table>
<tr>
<th>Member
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>WMT_CLIENT_CONNECT</td>
<td>A client has connected to the broadcast. The <i>dwType</i> parameter is WMT_TYPE_BINARY, and the <i>pValue</i> parameter points to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties">WM_CLIENT_PROPERTIES</a> structure.</td>
</tr>
<tr>
<td>WMT_CLIENT_DISCONNECT</td>
<td>A client has disconnected from the broadcast. The <i>dwType</i> parameter is WMT_TYPE_BINARY, and the <i>pValue</i> parameter points to a <b>WM_CLIENT_PROPERTIES</b> structure.</td>
</tr>
</table>
 

The following <b>WMT_STATUS</b> enumeration values can be passed to the callback by the indexer.

<table>
<tr>
<th>Member
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>WMT_ERROR</td>
<td>An error occurred in reading the file.</td>
</tr>
<tr>
<td>WMT_OPENED</td>
<td>The file has been opened for indexing.</td>
</tr>
<tr>
<td>WMT_STARTED</td>
<td>The indexer has started indexing the file. The <i>pValue</i> parameter points to a <b>QWORD</b> that indicates the starting timestamp. If it is -1 the starting timestamp is 0. When the value is any other negative number, it should be converted to a positive to give the starting timestamp.</td>
</tr>
<tr>
<td>WMT_STOPPED</td>
<td>The indexer has stopped indexing the file.</td>
</tr>
<tr>
<td>WMT_CLOSED</td>
<td>The indexer has closed the file.</td>
</tr>
<tr>
<td>WMT_INDEX_PROGRESS</td>
<td>Indicates the progress of the current indexing operation. The argument is a <b>DWORD</b> that indicates percentage completed, ranging from 0 to 100.</td>
</tr>
</table>
 

The following <b>WMT_STATUS</b> enumeration values can be passed to the callback by the backup restorer.

<table>
<tr>
<th>Member
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>WMT_BACKUPRESTORE_BEGIN</td>
<td>Sent when backing up or restoring licenses to indicate the process has started.</td>
</tr>
<tr>
<td>WMT_BACKUPRESTORE_END</td>
<td>Sent when backing up or restoring licenses to indicate the process has completed successfully.</td>
</tr>
<tr>
<td>WMT_BACKUPRESTORE_CONNECTING</td>
<td>Sent only when restoring licenses, to indicate the clients credentials are being validated.</td>
</tr>
<tr>
<td>WMT_BACKUPRESTORE_DISCONNECTING</td>
<td>Sent only when restoring licenses to indicate the clients credentials were validated successfully.</td>
</tr>
<tr>
<td>WMT_ERROR_WITHURL</td>
<td>Sent only when restoring licenses to indicate the client does not have the rights to do this.</td>
</tr>
<tr>
<td>WMT_RESTRICTED_LICENSE</td>
<td>Sent only when backing up licenses to indicate the licenses are restricted and cannot be backed up.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback Interface</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status">WMT_STATUS</a>