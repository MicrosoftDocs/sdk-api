---
UID: NN:wmsdkidl.IWMWriter
title: IWMWriter
author: windows-sdk-content
description: The IWMWriter interface is used to write ASF files.
old-location: wmformat\iwmwriter.htm
old-project: wmformat
ms.assetid: a194ef11-5203-4e85-af91-cdce0c53fe76
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMWriter, IWMWriter interface [windows Media Format], IWMWriter interface [windows Media Format],described, IWMWriterInterface, wmformat.iwmwriter, wmsdkidl/IWMWriter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriter interface


## -description



The <b>IWMWriter</b> interface is used to write ASF files. It includes methods for allocating buffers, setting and retrieving input properties, and setting profiles and output file names. The writer object exposes this interface. To create the writer object, call the <a href="https://msdn.microsoft.com/26d42213-40a1-4e2c-805b-c0803ee015b4">WMCreateWriter</a> function.




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
<a href="https://msdn.microsoft.com/b23b2364-fb36-479f-bf92-76a5bb4722de">AllocateSample</a>
</td>
<td align="left" width="63%">
Allocates a buffer that the application can use to supply samples to the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">BeginWriting</a>
</td>
<td align="left" width="63%">
Initializes the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/020e2c9d-9581-48c9-bc7b-a0e9e5a60c63">EndWriting</a>
</td>
<td align="left" width="63%">
Terminates the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Functionality removed. Always returns S_OK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cb3cd79-0640-4a3b-8e8b-d81df2ff749f">GetInputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of uncompressed input streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c058de81-a29a-4bcd-a819-3cdef11cae9f">GetInputFormat</a>
</td>
<td align="left" width="63%">
Retrieves possible media formats for the specified input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3afe9e8-e045-4329-b3e5-6026147322ad">GetInputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of format types supported by this input on the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2889a1a7-3111-4c13-b15a-659f519c22f6">GetInputProps</a>
</td>
<td align="left" width="63%">
Retrieves the media properties of a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15084a4d-06e8-4f74-9697-ced794d2cdae">SetInputProps</a>
</td>
<td align="left" width="63%">
Specifies the media properties of a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/352cf497-f7d6-41e8-bdbb-c59215b617a3">SetOutputFilename</a>
</td>
<td align="left" width="63%">
Specifies the name of the file to be written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a931896-c102-4b3b-a5a3-b3ef85b276b9">SetProfile</a>
</td>
<td align="left" width="63%">
Specifies the profile to use for the current writing task, using a pointer to an <b>IWMProfile</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/743212fd-a1e7-47c5-a220-c203cc2788e6">SetProfileByID</a>
</td>
<td align="left" width="63%">
Specifies the profile to use for the current writing task, identifying the profile by its globally unique identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba1cf121-1d01-4e90-9ab0-95af0b6e3850">WriteSample</a>
</td>
<td align="left" width="63%">
Passes in uncompressed data to be compressed and appended to the Windows Media file that is being created.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink Interface</a>



<a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink Interface</a>



<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>



<a href="https://msdn.microsoft.com/d722b676-bf65-4f91-8118-bb12d3bbb6cb">Writing ASF Files</a>
 

 

