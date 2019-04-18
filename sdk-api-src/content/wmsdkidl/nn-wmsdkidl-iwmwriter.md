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



The <b>IWMWriter</b> interface is used to write ASF files. It includes methods for allocating buffers, setting and retrieving input properties, and setting profiles and output file names. The writer object exposes this interface. To create the writer object, call the <a href="https://msdn.microsoft.com/en-us/library/Dd757789(v=VS.85).aspx">WMCreateWriter</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMWriter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757473(v=VS.85).aspx">AllocateSample</a>
</td>
<td align="left" width="63%">
Allocates a buffer that the application can use to supply samples to the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757474(v=VS.85).aspx">BeginWriting</a>
</td>
<td align="left" width="63%">
Initializes the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757475(v=VS.85).aspx">EndWriting</a>
</td>
<td align="left" width="63%">
Terminates the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757476(v=VS.85).aspx">Flush</a>
</td>
<td align="left" width="63%">
Functionality removed. Always returns S_OK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757477(v=VS.85).aspx">GetInputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of uncompressed input streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757478(v=VS.85).aspx">GetInputFormat</a>
</td>
<td align="left" width="63%">
Retrieves possible media formats for the specified input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757480(v=VS.85).aspx">GetInputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of format types supported by this input on the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757482(v=VS.85).aspx">GetInputProps</a>
</td>
<td align="left" width="63%">
Retrieves the media properties of a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757484(v=VS.85).aspx">SetInputProps</a>
</td>
<td align="left" width="63%">
Specifies the media properties of a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757506(v=VS.85).aspx">SetOutputFilename</a>
</td>
<td align="left" width="63%">
Specifies the name of the file to be written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757507(v=VS.85).aspx">SetProfile</a>
</td>
<td align="left" width="63%">
Specifies the profile to use for the current writing task, using a pointer to an <b>IWMProfile</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757508(v=VS.85).aspx">SetProfileByID</a>
</td>
<td align="left" width="63%">
Specifies the profile to use for the current writing task, identifying the profile by its globally unique identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757509(v=VS.85).aspx">WriteSample</a>
</td>
<td align="left" width="63%">
Passes in uncompressed data to be compressed and appended to the Windows Media file that is being created.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798720(v=VS.85).aspx">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798742(v=VS.85).aspx">IWMWriterFileSink Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798761(v=VS.85).aspx">IWMWriterNetworkSink Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>



<a href="https://msdn.microsoft.com/d722b676-bf65-4f91-8118-bb12d3bbb6cb">Writing ASF Files</a>
 

 

