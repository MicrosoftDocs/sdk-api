---
UID: NN:wmsdkidl.IWMReader
title: IWMReader (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReader interface is used to open, close, start, pause, resume, and unlock the WMReader object.
old-location: wmformat\iwmreader.htm
tech.root: wmformat
ms.assetid: e995b707-d388-4ec3-b3c8-b111628c13d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReader, IWMReader interface [windows Media Format], IWMReader interface [windows Media Format],described, IWMReaderInterface, wmformat.iwmreader, wmsdkidl/IWMReader
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
 - IWMReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReader interface


## -description



The <b>IWMReader</b> interface is used to open, close, start, pause, resume, and unlock the <b>WMReader</b> object. It is also used to stop reading files, and to get and set the output properties.

Many of the methods in this interface are asynchronous and send status notifications to the application through an <a href="https://msdn.microsoft.com/en-us/library/Dd798545(v=VS.85).aspx">IWMStatusCallback::OnStatus</a> method implemented in the application.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743588(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Deletes all outputs on the reader and releases the file resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743589(v=VS.85).aspx">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of uncompressed media streams sent from the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743592(v=VS.85).aspx">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves the supported formats for a specified output media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743593(v=VS.85).aspx">GetOutputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of format types supported by this output media stream on the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743595(v=VS.85).aspx">GetOutputProps</a>
</td>
<td align="left" width="63%">
Retrieves the current properties of an uncompressed output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743597(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens an ASF file for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743600(v=VS.85).aspx">Pause</a>
</td>
<td align="left" width="63%">
Pauses the current read operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743602(v=VS.85).aspx">Resume</a>
</td>
<td align="left" width="63%">
Restarts read operation from the current time offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743605(v=VS.85).aspx">SetOutputProps</a>
</td>
<td align="left" width="63%">
Specifies the properties of an uncompressed output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743608(v=VS.85).aspx">Start</a>
</td>
<td align="left" width="63%">
Starts reading from the current time offset. Uncompressed data is passed to <a href="https://msdn.microsoft.com/en-us/library/Dd743503(v=VS.85).aspx">IWMReaderCallback::OnSample</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743610(v=VS.85).aspx">Stop</a>
</td>
<td align="left" width="63%">
Stops reading, after which there is no current read position.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757447(v=VS.85).aspx">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743493(v=VS.85).aspx">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

