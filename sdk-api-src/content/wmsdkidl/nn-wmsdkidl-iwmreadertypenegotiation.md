---
UID: NN:wmsdkidl.IWMReaderTypeNegotiation
title: IWMReaderTypeNegotiation
author: windows-sdk-content
description: The IWMReaderTypeNegotiation interface provides a single method that can be used to test certain changes to the output properties of a stream.An IWMReaderTypeNegotiation interface exists for every reader object.
old-location: wmformat\iwmreadertypenegotiation.htm
old-project: wmformat
ms.assetid: 289ca857-5421-47f8-927e-6ca4204a31f9
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMReaderTypeNegotiation, IWMReaderTypeNegotiation interface [windows Media Format], IWMReaderTypeNegotiation interface [windows Media Format],described, IWMReaderTypeNegotiationInterface, wmformat.iwmreadertypenegotiation, wmsdkidl/IWMReaderTypeNegotiation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMReaderTypeNegotiation
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderTypeNegotiation interface


## -description



The <b>IWMReaderTypeNegotiation</b> interface provides a single method that can be used to test certain changes to the output properties of a stream.

An <b>IWMReaderTypeNegotiation</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderTypeNegotiation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderTypeNegotiation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderTypeNegotiation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87d16641-3d28-4bad-962b-8ec808cd7877">TryOutputProps</a>
</td>
<td align="left" width="63%">
Determines whether certain changes to the properties of an output are possible.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

