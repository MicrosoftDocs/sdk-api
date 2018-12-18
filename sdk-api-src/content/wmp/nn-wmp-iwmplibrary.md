---
UID: NN:wmp.IWMPLibrary
title: IWMPLibrary
author: windows-sdk-content
description: The IWMPLibrary interface represents a library.
old-location: wmp\iwmplibrary.htm
tech.root: WMP
ms.assetid: add0ed43-d83f-4793-b1f6-ccad0f01854c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPLibrary, IWMPLibrary interface [Windows Media Player], IWMPLibrary interface [Windows Media Player],described, IWMPLibraryInterface, wmp.iwmplibrary, wmp/IWMPLibrary
ms.topic: interface
req.header: wmp.h
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
 - wmp.h
api_name:
 - IWMPLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPLibrary interface


## -description



The <b>IWMPLibrary</b> interface represents a library.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPLibrary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563392(v=VS.85).aspx">get_mediaCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IWMPMediacollection</b> interface for the current library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563393(v=VS.85).aspx">get_name</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the current library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563394(v=VS.85).aspx">get_type</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the library type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563395(v=VS.85).aspx">isIdentical</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the supplied object is the same as the current one.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563386(v=VS.85).aspx">IWMPLibraryServices::getLibraryByType</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

