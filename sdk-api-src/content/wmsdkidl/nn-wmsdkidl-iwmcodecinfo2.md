---
UID: NN:wmsdkidl.IWMCodecInfo2
title: IWMCodecInfo2 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMCodecInfo2 interface manages the retrieval of information about codecs. To access it, call QueryInterface on a profile manager object.
old-location: wmformat\iwmcodecinfo2.htm
tech.root: wmformat
ms.assetid: 0cfb355e-af68-400d-aa64-57f17e7d936b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMCodecInfo2, IWMCodecInfo2 interface [windows Media Format], IWMCodecInfo2 interface [windows Media Format],described, IWMCodecInfo2Interface, wmformat.iwmcodecinfo2, wmsdkidl/IWMCodecInfo2
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
 - IWMCodecInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMCodecInfo2 interface


## -description



The <b>IWMCodecInfo2</b> interface manages the retrieval of information about codecs. To access it, call <b>QueryInterface</b> on a profile manager object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecInfo2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd743313(v=VS.85).aspx">IWMCodecInfo</a>. <b>IWMCodecInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743315(v=VS.85).aspx">GetCodecFormatDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of a specified codec format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743316(v=VS.85).aspx">GetCodecName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a specified codec.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd743313(v=VS.85).aspx">IWMCodecInfo</a>
</td>
<td>IID_IWMCodecInfo</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd743317(v=VS.85).aspx">IWMCodecInfo3</a>
</td>
<td>IID_IWMCodecInfo3</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757385(v=VS.85).aspx">IWMProfileManager</a>
</td>
<td>IID_IWMProfileManager</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757386(v=VS.85).aspx">IWMProfileManager2</a>
</td>
<td>IID_IWMProfileManager2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757389(v=VS.85).aspx">IWMProfileManagerLanguage</a>
</td>
<td>IID_IWMProfileManagerLanguage</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743313(v=VS.85).aspx">IWMCodecInfo Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757385(v=VS.85).aspx">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

