---
UID: NN:wmsdkidl.IWMReaderAdvanced3
title: IWMReaderAdvanced3 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderAdvanced3 interface provides additional functionality to the reader object.
old-location: wmformat\iwmreaderadvanced3.htm
tech.root: wmformat
ms.assetid: 20bf3c00-0f35-4b8e-b78d-a36fbfd865b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderAdvanced3, IWMReaderAdvanced3 interface [windows Media Format], IWMReaderAdvanced3 interface [windows Media Format],described, IWMReaderAdvanced3Interface, wmformat.iwmreaderadvanced3, wmsdkidl/IWMReaderAdvanced3
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
 - IWMReaderAdvanced3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced3 interface


## -description



The <b>IWMReaderAdvanced3</b> interface provides additional functionality to the reader object. It contains methods that enhance the ability to playback a file.

<b>IWMReaderAdvanced3</b> exists for each instance of the reader objects created with the <b>WMCreateReader</b> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2</a>. <b>IWMReaderAdvanced3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757448(v=VS.85).aspx">StartAtPosition</a>
</td>
<td align="left" width="63%">
Provides the ability to specify a starting position using a variety of offsets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757449(v=VS.85).aspx">StopNetStreaming</a>
</td>
<td align="left" width="63%">
Stops network streaming while received packets continue to be delivered.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757460(v=VS.85).aspx">IWMReaderAdvanced5 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757462(v=VS.85).aspx">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

