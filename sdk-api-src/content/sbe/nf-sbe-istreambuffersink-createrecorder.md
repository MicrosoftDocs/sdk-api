---
UID: NF:sbe.IStreamBufferSink.CreateRecorder
title: IStreamBufferSink::CreateRecorder (sbe.h)
author: windows-sdk-content
description: This topic applies only to Windows XP Service Pack 1 or later.
old-location: mstv\istreambuffersink_createrecorder.htm
tech.root: mstv
ms.assetid: a9f3b7e1-4f54-4802-af24-4b791ee646fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateRecorder, CreateRecorder method [Microsoft TV Technologies], CreateRecorder method [Microsoft TV Technologies],IStreamBufferSink interface, IStreamBufferSink interface [Microsoft TV Technologies],CreateRecorder method, IStreamBufferSink.CreateRecorder, IStreamBufferSink::CreateRecorder, IStreamBufferSinkCreateRecorder, mstv.istreambuffersink_createrecorder, sbe/IStreamBufferSink::CreateRecorder
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferSink.CreateRecorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferSink::CreateRecorder


## -description



This topic applies only to Windows XP Service Pack 1 or later.
        



The <b>CreateRecorder</b> method creates a new Recording object. Recording objects are used to create permanent files from the stream buffer.


## -parameters




### -param pszFilename [in]

Pointer to a null-terminated wide-character string that contains the file name for the recording.


### -param dwRecordType [in]

Indicates the type of recording to create, either a reference recording or a content recording. Specify one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>RECORDING_TYPE_REFERENCE</td>
<td>Reference recording. A reference recording is created from temporary backing files that have already been recorded. It uses a stub file to reference the existing files. Because a reference recording refers to existing content, the start time can be in the past.</td>
</tr>
<tr>
<td>RECORDING_TYPE_CONTENT</td>
<td>Content recording. A content recording saves content into a new file. Because the content must be new, the start time cannot be in the past.</td>
</tr>
</table>
 


### -param pRecordingIUnknown [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/717a3b99-d998-4e64-aab6-6b06e18991da">Recording</a> object's <b>IUnknown</b> interface.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The Stream Buffer Sink filter's profile must be locked, either explicitly or implicitly, before you call this method. For more information, see <a href="https://msdn.microsoft.com/9e694cc2-090e-43b1-88c7-77175a930bf1">IStreamBufferSink::LockProfile</a>.

The returned <b>IUnknown</b> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/1aee15a3-5bc8-401b-9b37-b9351fd7c91f">Creating Stream Buffer Recordings</a>



<a href="https://msdn.microsoft.com/4ae5a9e9-da51-4034-9a2c-22b57374deac">IStreamBufferSink Interface</a>
 

 

