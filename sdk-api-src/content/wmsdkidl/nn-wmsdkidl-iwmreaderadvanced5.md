---
UID: NN:wmsdkidl.IWMReaderAdvanced5
title: IWMReaderAdvanced5 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderAdvanced5 interface enables you to associate a player-hook callback interface with the reader object.An IWMReaderAdvanced5 interface exists for every reader object.
old-location: wmformat\iwmreaderadvanced5.htm
tech.root: wmformat
ms.assetid: 28d697d8-99b5-4968-a765-ba01b86914f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced5, IWMReaderAdvanced5 interface [windows Media Format], IWMReaderAdvanced5 interface [windows Media Format],described, IWMReaderAdvanced5Interface, wmformat.iwmreaderadvanced5, wmsdkidl/IWMReaderAdvanced5
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
 - IWMReaderAdvanced5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced5 interface


## -description



The <b>IWMReaderAdvanced5</b> interface enables you to associate a player-hook callback interface with the reader object.

An <b>IWMReaderAdvanced5</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced5</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4</a>. <b>IWMReaderAdvanced5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757461(v=VS.85).aspx">SetPlayerHook</a>
</td>
<td align="left" width="63%">
Sets the player hook callback interface that the reader calls before processing samples by using DirectX Video Acceleration.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -remarks



A player-hook callback can be assigned in the reader object to enable per-sample processing when using DirectX Video Acceleration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757447(v=VS.85).aspx">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757462(v=VS.85).aspx">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

