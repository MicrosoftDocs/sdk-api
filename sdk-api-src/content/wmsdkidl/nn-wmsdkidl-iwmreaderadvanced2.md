---
UID: NN:wmsdkidl.IWMReaderAdvanced2
title: IWMReaderAdvanced2
author: windows-sdk-content
description: The IWMReaderAdvanced2 interface provides additional advanced methods for a reader object.
old-location: wmformat\iwmreaderadvanced2.htm
old-project: wmformat
ms.assetid: 5d741e49-9fdf-4f8d-9ea1-faaecf879be4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderAdvanced2, IWMReaderAdvanced2 interface [windows Media Format], IWMReaderAdvanced2 interface [windows Media Format],described, IWMReaderAdvanced2Interface, wmformat.iwmreaderadvanced2, wmsdkidl/IWMReaderAdvanced2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.redist: 
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
 - IWMReaderAdvanced2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced2 interface


## -description



The <b>IWMReaderAdvanced2</b> interface provides additional advanced methods for a reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced2</b> interface inherits from <a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced</a>. <b>IWMReaderAdvanced2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e0419f53-9962-4d81-9153-0538c60861eb">GetBufferProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of data that has been buffered, and the time remaining to completion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06bff83f-c3f2-4eca-85dd-7e7b93cfd73d">GetDownloadProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage and amount of data that has been downloaded, and the time remaining to completion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/034ad344-2266-4662-9797-70031f58f0cd">GetLogClientID</a>
</td>
<td align="left" width="63%">
Queries whether the reader logs the client's unique ID or an anonymous session ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a46da973-8f2f-48b8-9a74-d54e67f68a83">GetOutputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular output by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45c7e2c2-fff4-41a9-b5ce-76d8d6257e77">GetPlayMode</a>
</td>
<td align="left" width="63%">
Retrieves the current play mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/056d5f3f-79bf-4e21-9f2c-cda05eaca13d">GetProtocolName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the protocol that is currently being used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0317f010-4b7f-4f79-9460-ba6b1e904ffa">GetSaveAsProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of data that has been saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20822e1d-b367-4b03-9d8a-985427f0062d">OpenStream</a>
</td>
<td align="left" width="63%">
Opens a Windows Media stream for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c216adf1-390c-45cc-acae-645fe29f55de">Preroll</a>
</td>
<td align="left" width="63%">
Begins prerolling the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97bdac1f-8830-45c0-9229-322ad72b3954">SaveFileAs</a>
</td>
<td align="left" width="63%">
Saves the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/818b7a0e-bbf4-42b2-a5a4-75078834c9f6">SetLogClientID</a>
</td>
<td align="left" width="63%">
Specifies whether the reader logs the client's unique ID or an anonymous session ID..

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/035a74d2-288d-4754-8cb2-4508b7fe4649">SetOutputSetting</a>
</td>
<td align="left" width="63%">
Specifies a named setting for a particular output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b20a0c-fedf-46d4-a76b-7596dcf8fcf8">SetPlayMode</a>
</td>
<td align="left" width="63%">
Specifies the current play mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/444adb2f-4289-4950-8841-07353479ef43">StartAtMarker</a>
</td>
<td align="left" width="63%">
Starts the reader from a specified <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">marker</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c380a68-d86c-421a-8102-019848893c35">StopBuffering</a>
</td>
<td align="left" width="63%">
Requests that the reader stops buffering as soon as possible.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/20bf3c00-0f35-4b8e-b78d-a36fbfd865b7">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/28d697d8-99b5-4968-a765-ba01b86914f6">IWMReaderAdvanced5 Interface</a>



<a href="https://msdn.microsoft.com/95e8c151-9aae-4930-824c-8809dfc07705">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

