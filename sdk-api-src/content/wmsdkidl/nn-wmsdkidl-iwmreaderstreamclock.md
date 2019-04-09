---
UID: NN:wmsdkidl.IWMReaderStreamClock
title: IWMReaderStreamClock (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderStreamClock interface provides access to the clock used by the reader.This interface exists for every reader object.
old-location: wmformat\iwmreaderstreamclock.htm
tech.root: wmformat
ms.assetid: 0f170b6d-fd93-4bf8-8a98-f2a80f03b380
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderStreamClock, IWMReaderStreamClock interface [windows Media Format], IWMReaderStreamClock interface [windows Media Format],described, IWMReaderStreamClockInterface, wmformat.iwmreaderstreamclock, wmsdkidl/IWMReaderStreamClock
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
 - IWMReaderStreamClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderStreamClock interface


## -description



The <b>IWMReaderStreamClock</b> interface provides access to the clock used by the reader.

This interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderStreamClock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderStreamClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderStreamClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743568(v=VS.85).aspx">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the stream clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743570(v=VS.85).aspx">KillTimer</a>
</td>
<td align="left" width="63%">
Cancels a timer on the stream clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743573(v=VS.85).aspx">SetTimer</a>
</td>
<td align="left" width="63%">
Sets a timer on the stream clock.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

