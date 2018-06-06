---
UID: NN:wmsdkidl.IWMReader
title: IWMReader
author: windows-sdk-content
description: The IWMReader interface is used to open, close, start, pause, resume, and unlock the WMReader object.
old-location: wmformat\iwmreader.htm
old-project: wmformat
ms.assetid: e995b707-d388-4ec3-b3c8-b111628c13d7
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMReader, IWMReader interface [windows Media Format], IWMReader interface [windows Media Format],described, IWMReaderInterface, wmformat.iwmreader, wmsdkidl/IWMReader
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
 - IWMReader
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReader interface


## -description



The <b>IWMReader</b> interface is used to open, close, start, pause, resume, and unlock the <b>WMReader</b> object. It is also used to stop reading files, and to get and set the output properties.

Many of the methods in this interface are asynchronous and send status notifications to the application through an <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method implemented in the application.




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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Deletes all outputs on the reader and releases the file resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f04fad9-a638-45c6-b924-50f57472dfe3">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of uncompressed media streams sent from the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e73d13b9-3fca-4de1-b89d-5cacc6311cd3">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves the supported formats for a specified output media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/282c5fb6-6b8a-4a13-8a20-4926c6f68800">GetOutputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of format types supported by this output media stream on the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8958abd0-cc2b-4d02-a831-c998d468fb06">GetOutputProps</a>
</td>
<td align="left" width="63%">
Retrieves the current properties of an uncompressed output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens an ASF file for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses the current read operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4af00d1f-c78a-4f43-be2d-9561e3c7cf36">Resume</a>
</td>
<td align="left" width="63%">
Restarts read operation from the current time offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a5325d1-880b-4d65-96af-9d311dca989b">SetOutputProps</a>
</td>
<td align="left" width="63%">
Specifies the properties of an uncompressed output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts reading from the current time offset. Uncompressed data is passed to <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops reading, after which there is no current read position.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/20bf3c00-0f35-4b8e-b78d-a36fbfd865b7">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

