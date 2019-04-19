---
UID: NN:wmsdkidl.IWMReaderAdvanced4
title: IWMReaderAdvanced4 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderAdvanced4 interface provides additional functionality to the reader.An IWMReaderAdvanced4 interface exists for every reader object.
old-location: wmformat\iwmreaderadvanced4.htm
tech.root: wmformat
ms.assetid: 56695c57-f6c5-4c57-b3d4-73d169b379fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced4, IWMReaderAdvanced4 interface [windows Media Format], IWMReaderAdvanced4 interface [windows Media Format],described, IWMReaderAdvanced4Interface, wmformat.iwmreaderadvanced4, wmsdkidl/IWMReaderAdvanced4
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
 - IWMReaderAdvanced4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced4 interface


## -description



The <b>IWMReaderAdvanced4</b> interface provides additional functionality to the reader.

An <b>IWMReaderAdvanced4</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced4</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757447(v=VS.85).aspx">IWMReaderAdvanced3</a>. <b>IWMReaderAdvanced4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757451(v=VS.85).aspx">AddLogParam</a>
</td>
<td align="left" width="63%">
Adds a named value to the logging information that the reader object will send to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757452(v=VS.85).aspx">CancelSaveFileAs</a>
</td>
<td align="left" width="63%">
Cancels a file save in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757453(v=VS.85).aspx">CanSaveFileAs</a>
</td>
<td align="left" width="63%">
Determines whether content being read by the reader object can be saved using the <a href="https://msdn.microsoft.com/en-us/library/Dd757440(v=VS.85).aspx">IWMReaderAdvanced2::SaveFileAs</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757454(v=VS.85).aspx">GetLanguage</a>
</td>
<td align="left" width="63%">
Retrieves information about a language supported by an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757455(v=VS.85).aspx">GetLanguageCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of languages supported by an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757456(v=VS.85).aspx">GetMaxSpeedFactor</a>
</td>
<td align="left" width="63%">
Retrieves the maximum playback rate that can be delivered by the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757457(v=VS.85).aspx">GetURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL of the file being read.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757458(v=VS.85).aspx">IsUsingFastCache</a>
</td>
<td align="left" width="63%">
Queries whether the reader is using Fast Cache streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757459(v=VS.85).aspx">SendLogParams</a>
</td>
<td align="left" width="63%">
Sends log entries to the originating server.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757447(v=VS.85).aspx">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757460(v=VS.85).aspx">IWMReaderAdvanced5 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757462(v=VS.85).aspx">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

