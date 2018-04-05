---
UID: NN:wmsdkidl.IWMPacketSize2
title: IWMPacketSize2
author: windows-driver-content
description: The IWMPacketSize2 interface provides methods to set and retrieve the minimum packet size for a profile.An IWMPacketSize2 interface can be obtained for either a profile object, a reader object, or a synchronous reader object.
old-location: wmformat\iwmpacketsize2.htm
old-project: wmformat
ms.assetid: 4af4c088-9fc3-46a9-8451-518b11bc94e3
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMPacketSize2, IWMPacketSize2 interface [windows Media Format], IWMPacketSize2 interface [windows Media Format], described, IWMPacketSize2Interface, wmformat.iwmpacketsize2, wmsdkidl/IWMPacketSize2
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
-	IWMPacketSize2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPacketSize2 interface


## -description



The <b>IWMPacketSize2</b> interface provides methods to set and retrieve the minimum <a href="wmformat_glossary.htm">packet</a> size for a profile.

An <b>IWMPacketSize2</b> interface can be obtained for either a profile object, a reader object, or a synchronous reader object. You can obtain a pointer to <b>IWMPacketSize2</b> by calling the <b>QueryInterface</b> method of any of the other interfaces in one of the supported objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPacketSize2</b> interface inherits from <a href="https://msdn.microsoft.com/002442fe-46de-49d9-8aff-ad7c9aabc8d1">IWMPacketSize</a>. <b>IWMPacketSize2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPacketSize2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b15f5b9-b7c1-4427-81d9-bbcd0bb0ce45">GetMinPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum packet size for files created with the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d58da65-710c-46ea-8fb9-9d161df06483">SetMinPacketSize</a>
</td>
<td align="left" width="63%">
Sets the minimum packet size for files created with the profile.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/002442fe-46de-49d9-8aff-ad7c9aabc8d1">IWMPacketSize Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/ec42889e-580e-4a65-9fe6-4a5f15c97eb0">Profile Object</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>
 

 

