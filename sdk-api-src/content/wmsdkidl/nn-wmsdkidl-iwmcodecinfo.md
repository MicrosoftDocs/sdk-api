---
UID: NN:wmsdkidl.IWMCodecInfo
title: IWMCodecInfo
author: windows-sdk-content
description: The IWMCodecInfo interface retrieves the number and types of codecs available.
old-location: wmformat\iwmcodecinfo.htm
tech.root: wmformat
ms.assetid: 70661d13-737a-4e83-94e6-9a1af07b0369
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMCodecInfo, IWMCodecInfo interface [windows Media Format], IWMCodecInfo interface [windows Media Format],described, IWMCodecInfoInterface, wmformat.iwmcodecinfo, wmsdkidl/IWMCodecInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMCodecInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMCodecInfo interface


## -description



The <b>IWMCodecInfo</b> interface retrieves the number and types of codecs available. You can use this interface to get information about supported compressed data formats for creating custom profiles.

Individual codec formats exist only for audio codecs. The characteristics of compressed video will vary based upon the frame size and color depth of the original digital media and, therefore, cannot be predicted until the time of encoding.

An <b>IWMCodecInfo</b> interface exists for each profile manager object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the profile manager object, typically <b>IWMProfileManager</b>.

The methods of the <b>IWMCodecInfo</b> interface are inherited by <b>IWMCodecInfo2</b> and <b>IWMCodecInfo3</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMCodecInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743322(v=VS.85).aspx">GetCodecFormat</a>
</td>
<td align="left" width="63%">
Retrieves a structure describing the format of a specified codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743323(v=VS.85).aspx">GetCodecFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of formats supported by the specified codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743324(v=VS.85).aspx">GetCodecInfoCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of supported codecs.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd743314(v=VS.85).aspx">IWMCodecInfo2</a>
</td>
<td>IID_IWMCodecInfo2</td>
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




<a href="https://msdn.microsoft.com/en-us/library/Dd743314(v=VS.85).aspx">IWMCodecInfo2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743317(v=VS.85).aspx">IWMCodecInfo3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757385(v=VS.85).aspx">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

