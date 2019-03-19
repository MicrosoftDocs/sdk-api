---
UID: NN:wmsdkidl.IWMReaderAdvanced6
title: IWMReaderAdvanced6 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderAdvanced6 interface enables sample protection.An IWMReaderAdvanced6 interface exists for every reader object.
old-location: wmformat\iwmreaderadvanced6.htm
tech.root: wmformat
ms.assetid: 95e8c151-9aae-4930-824c-8809dfc07705
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderAdvanced6, IWMReaderAdvanced6 interface [windows Media Format], IWMReaderAdvanced6 interface [windows Media Format],described, IWMReaderAdvanced6Interface, wmformat.iwmreaderadvanced6, wmsdkidl/IWMReaderAdvanced6
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
 - IWMReaderAdvanced6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced6 interface


## -description



The <b>IWMReaderAdvanced6</b> interface enables sample protection.

An <b>IWMReaderAdvanced6</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced6</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757460(v=VS.85).aspx">IWMReaderAdvanced5</a>. <b>IWMReaderAdvanced6</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced6</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757463(v=VS.85).aspx">SetProtectStreamSamples</a>
</td>
<td align="left" width="63%">
Configures sample protection.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757447(v=VS.85).aspx">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757460(v=VS.85).aspx">IWMReaderAdvanced5 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

