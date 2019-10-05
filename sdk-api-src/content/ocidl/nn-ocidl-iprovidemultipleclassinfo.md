---
UID: NN:ocidl.IProvideMultipleClassInfo
title: IProvideMultipleClassInfo (ocidl.h)
author: windows-sdk-content
description: An extension to IProvideClassInfo2 that makes it faster and easier to retrieve type information from a component that may have multiple coclasses that determine its behavior.
old-location: com\iprovidemultipleclassinfo.htm
tech.root: com
ms.assetid: 87407830-b34b-4d4e-a5cc-551f47cffb75
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProvideMultipleClassInfo, IProvideMultipleClassInfo interface [COM], IProvideMultipleClassInfo interface [COM],described, _com_iprovidemultipleclassinfo, com.iprovidemultipleclassinfo, ocidl/IProvideMultipleClassInfo
ms.topic: interface
f1_keywords: 
 - "ocidl/IProvideMultipleClassInfo"
dev_langs:
 - c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IProvideMultipleClassInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProvideMultipleClassInfo interface


## -description


An extension to <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo2">IProvideClassInfo2</a> that makes it faster and easier to retrieve type information from a component that may have multiple coclasses that determine its behavior. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideMultipleClassInfo</b> interface inherits from <b>IProvideClassInfo2</b>. <b>IProvideMultipleClassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProvideMultipleClassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iprovidemultipleclassinfo-getinfoofindex">GetInfoOfIndex</a>
</td>
<td align="left" width="63%">
Retrieves the type information from the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iprovidemultipleclassinfo-getmultitypeinfocount">GetMultiTypeInfoCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of type information blocks that this object must provide.

</td>
</tr>
</table> 

