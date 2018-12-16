---
UID: NN:wmsdkidl.IWMReaderAdvanced2
title: IWMReaderAdvanced2
author: windows-sdk-content
description: The IWMReaderAdvanced2 interface provides additional advanced methods for a reader object.
old-location: wmformat\iwmreaderadvanced2.htm
tech.root: wmformat
ms.assetid: 5d741e49-9fdf-4f8d-9ea1-faaecf879be4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderAdvanced2, IWMReaderAdvanced2 interface [windows Media Format], IWMReaderAdvanced2 interface [windows Media Format],described, IWMReaderAdvanced2Interface, wmformat.iwmreaderadvanced2, wmsdkidl/IWMReaderAdvanced2
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
 - IWMReaderAdvanced2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced2 interface


## -description



The <b>IWMReaderAdvanced2</b> interface provides additional advanced methods for a reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced</a>. <b>IWMReaderAdvanced2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757431(v=VS.85).aspx">GetBufferProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of data that has been buffered, and the time remaining to completion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757432(v=VS.85).aspx">GetDownloadProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage and amount of data that has been downloaded, and the time remaining to completion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757433(v=VS.85).aspx">GetLogClientID</a>
</td>
<td align="left" width="63%">
Queries whether the reader logs the client's unique ID or an anonymous session ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757434(v=VS.85).aspx">GetOutputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular output by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757435(v=VS.85).aspx">GetPlayMode</a>
</td>
<td align="left" width="63%">
Retrieves the current play mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757436(v=VS.85).aspx">GetProtocolName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the protocol that is currently being used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757437(v=VS.85).aspx">GetSaveAsProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of data that has been saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757438(v=VS.85).aspx">OpenStream</a>
</td>
<td align="left" width="63%">
Opens a Windows Media stream for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757439(v=VS.85).aspx">Preroll</a>
</td>
<td align="left" width="63%">
Begins prerolling the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757440(v=VS.85).aspx">SaveFileAs</a>
</td>
<td align="left" width="63%">
Saves the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757441(v=VS.85).aspx">SetLogClientID</a>
</td>
<td align="left" width="63%">
Specifies whether the reader logs the client's unique ID or an anonymous session ID..

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757442(v=VS.85).aspx">SetOutputSetting</a>
</td>
<td align="left" width="63%">
Specifies a named setting for a particular output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757443(v=VS.85).aspx">SetPlayMode</a>
</td>
<td align="left" width="63%">
Specifies the current play mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757445(v=VS.85).aspx">StartAtMarker</a>
</td>
<td align="left" width="63%">
Starts the reader from a specified <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">marker</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757446(v=VS.85).aspx">StopBuffering</a>
</td>
<td align="left" width="63%">
Requests that the reader stops buffering as soon as possible.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757447(v=VS.85).aspx">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757460(v=VS.85).aspx">IWMReaderAdvanced5 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757462(v=VS.85).aspx">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

