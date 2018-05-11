---
UID: NN:wmsdkidl.IWMCodecInfo3
title: IWMCodecInfo3
author: windows-driver-content
description: The IWMCodecInfo3 interface retrieves properties from a codec.You can retrieve a pointer to IWMCodecInfo3 with a call to the QueryInterface method of any other interface of the profile manager object.
old-location: wmformat\iwmcodecinfo3.htm
old-project: wmformat
ms.assetid: fd882612-1f60-4b51-a180-0d34d78c99dd
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMCodecInfo3, IWMCodecInfo3 interface [windows Media Format], IWMCodecInfo3 interface [windows Media Format],described, IWMCodecInfo3Interface, wmformat.iwmcodecinfo3, wmsdkidl/IWMCodecInfo3
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMCodecInfo3
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecInfo3 interface


## -description



The <b>IWMCodecInfo3</b> interface retrieves properties from a codec.

You can retrieve a pointer to <b>IWMCodecInfo3</b> with a call to the <b>QueryInterface</b> method of any other interface of the profile manager object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecInfo3</b> interface inherits from <a href="https://msdn.microsoft.com/0cfb355e-af68-400d-aa64-57f17e7d936b">IWMCodecInfo2</a>. <b>IWMCodecInfo3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9a8f34ef-4d52-47d4-b6d5-e6f07f27cc8d">GetCodecEnumerationSetting</a>
</td>
<td align="left" width="63%">
Obtains the current value for a codec enumeration setting. Codec enumeration settings enable you to enumerate codec formats by feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04f5301f-0033-4cf3-bc05-3159fe274a8d">GetCodecFormatProp</a>
</td>
<td align="left" width="63%">
Retrieves a property from one format of a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/444f5789-c5e5-4eeb-a2b4-11f959641206">GetCodecProp</a>
</td>
<td align="left" width="63%">
Retrieves a codec property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b4883b8-63c0-40ff-b13f-303d30ebfe15">SetCodecEnumerationSetting</a>
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
<a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo</a>
</td>
<td>IID_IWMCodecInfo</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0cfb355e-af68-400d-aa64-57f17e7d936b">IWMCodecInfo2</a>
</td>
<td>IID_IWMCodecInfo2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/002442fe-46de-49d9-8aff-ad7c9aabc8d1">IWMPacketSize</a>
</td>
<td>IID_IWMPacketSize</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4af4c088-9fc3-46a9-8451-518b11bc94e3">IWMPacketSize2</a>
</td>
<td>IID_IWMPacketSize2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager</a>
</td>
<td>IID_IWMProfileManager</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/eb5d904e-15ee-4066-ab05-c4e133bc89d7">IWMProfileManager2</a>
</td>
<td>IID_IWMProfileManager2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54875162-65fe-4959-b567-38c17ba2894d">IWMProfileManagerLanguage</a>
</td>
<td>IID_IWMProfileManagerLanguage</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo Interface</a>



<a href="https://msdn.microsoft.com/0cfb355e-af68-400d-aa64-57f17e7d936b">IWMCodecInfo2 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

