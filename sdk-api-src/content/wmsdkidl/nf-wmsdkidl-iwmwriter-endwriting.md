---
UID: NF:wmsdkidl.IWMWriter.EndWriting
title: IWMWriter::EndWriting
author: windows-sdk-content
description: The EndWriting method performs tasks required at the end of a writing session.
old-location: wmformat\iwmwriter_endwriting.htm
old-project: wmformat
ms.assetid: 020e2c9d-9581-48c9-bc7b-a0e9e5a60c63
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EndWriting, EndWriting method [windows Media Format], EndWriting method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],EndWriting method, IWMWriter.EndWriting, IWMWriter::EndWriting, IWMWriterEndWriting, wmformat.iwmwriter_endwriting, wmsdkidl/IWMWriter::EndWriting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMWriter.EndWriting
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriter::EndWriting


## -description



The <b>EndWriting</b> method performs tasks required at the end of a writing session. This method flushes the buffers, updates indices and headers, and closes the file. You must call <b>EndWriting</b> when you have finished sending samples to the writer to encode an ASF file.




## -parameters






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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The writer cannot currently be run.

</td>
</tr>
</table>
 




## -remarks



This method will not return a failure code if the disk space was used up before the encoding was completed. In order to be notified of a file writing error, an application should implement the <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a> method and listen for the NS_E_FILE_WRITE event.




## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a>
 

 

