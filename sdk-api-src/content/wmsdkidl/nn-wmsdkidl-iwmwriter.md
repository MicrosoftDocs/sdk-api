---
UID: NN:wmsdkidl.IWMWriter
title: IWMWriter (wmsdkidl.h)
author: windows-sdk-content
description: The IWMWriter interface is used to write ASF files.
old-location: wmformat\iwmwriter.htm
tech.root: wmformat
ms.assetid: a194ef11-5203-4e85-af91-cdce0c53fe76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMWriter, IWMWriter interface [windows Media Format], IWMWriter interface [windows Media Format],described, IWMWriterInterface, wmformat.iwmwriter, wmsdkidl/IWMWriter
ms.topic: interface
f1_keywords: ["wmsdkidl/IWMWriter"]
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - wmsdkidl.h
api_name:
 - IWMWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriter interface


## -description



The <b>IWMWriter</b> interface is used to write ASF files. It includes methods for allocating buffers, setting and retrieving input properties, and setting profiles and output file names. The writer object exposes this interface. To create the writer object, call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriter">WMCreateWriter</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample">AllocateSample</a>
</td>
<td align="left" width="63%">
Allocates a buffer that the application can use to supply samples to the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">BeginWriting</a>
</td>
<td align="left" width="63%">
Initializes the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting">EndWriting</a>
</td>
<td align="left" width="63%">
Terminates the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-flush">Flush</a>
</td>
<td align="left" width="63%">
Functionality removed. Always returns S_OK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount">GetInputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of uncompressed input streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat">GetInputFormat</a>
</td>
<td align="left" width="63%">
Retrieves possible media formats for the specified input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount">GetInputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of format types supported by this input on the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops">GetInputProps</a>
</td>
<td align="left" width="63%">
Retrieves the media properties of a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops">SetInputProps</a>
</td>
<td align="left" width="63%">
Specifies the media properties of a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename">SetOutputFilename</a>
</td>
<td align="left" width="63%">
Specifies the name of the file to be written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile">SetProfile</a>
</td>
<td align="left" width="63%">
Specifies the profile to use for the current writing task, using a pointer to an <b>IWMProfile</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid">SetProfileByID</a>
</td>
<td align="left" width="63%">
Specifies the profile to use for the current writing task, identifying the profile by its globally unique identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-writesample">WriteSample</a>
</td>
<td align="left" width="63%">
Passes in uncompressed data to be compressed and appended to the Windows Media file that is being created.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writing-asf-files">Writing ASF Files</a>
 

 

