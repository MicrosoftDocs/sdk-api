---
UID: NN:wmsdkidl.IWMCodecInfo3
title: IWMCodecInfo3 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMCodecInfo3 interface retrieves properties from a codec.You can retrieve a pointer to IWMCodecInfo3 with a call to the QueryInterface method of any other interface of the profile manager object.
old-location: wmformat\iwmcodecinfo3.htm
tech.root: wmformat
ms.assetid: fd882612-1f60-4b51-a180-0d34d78c99dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMCodecInfo3, IWMCodecInfo3 interface [windows Media Format], IWMCodecInfo3 interface [windows Media Format],described, IWMCodecInfo3Interface, wmformat.iwmcodecinfo3, wmsdkidl/IWMCodecInfo3
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
 - IWMCodecInfo3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecInfo3 interface


## -description



The <b>IWMCodecInfo3</b> interface retrieves properties from a codec.

You can retrieve a pointer to <b>IWMCodecInfo3</b> with a call to the <b>QueryInterface</b> method of any other interface of the profile manager object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecInfo3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd743314(v=VS.85).aspx">IWMCodecInfo2</a>. <b>IWMCodecInfo3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecInfo3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743318(v=VS.85).aspx">GetCodecEnumerationSetting</a>
</td>
<td align="left" width="63%">
Obtains the current value for a codec enumeration setting. Codec enumeration settings enable you to enumerate codec formats by feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743319(v=VS.85).aspx">GetCodecFormatProp</a>
</td>
<td align="left" width="63%">
Retrieves a property from one format of a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743320(v=VS.85).aspx">GetCodecProp</a>
</td>
<td align="left" width="63%">
Retrieves a codec property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743321(v=VS.85).aspx">SetCodecEnumerationSetting</a>
</td>
<td align="left" width="63%">
Sets a codec enumeration setting. Codec enumeration settings enable you to enumerate codec formats by feature.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd743314(v=VS.85).aspx">IWMCodecInfo2</a>
</td>
<td>IID_IWMCodecInfo2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757255(v=VS.85).aspx">IWMPacketSize</a>
</td>
<td>IID_IWMPacketSize</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757256(v=VS.85).aspx">IWMPacketSize2</a>
</td>
<td>IID_IWMPacketSize2</td>
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



<a href="https://msdn.microsoft.com/en-us/library/Dd743314(v=VS.85).aspx">IWMCodecInfo2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

