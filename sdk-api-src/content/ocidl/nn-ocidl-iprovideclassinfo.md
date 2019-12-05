---
UID: NN:ocidl.IProvideClassInfo
title: IProvideClassInfo (ocidl.h)
description: Provides access to the type information for an object's coclass entry in its type library.
old-location: com\iprovideclassinfo.htm
tech.root: com
ms.assetid: 867bfd3e-b2d8-4bbe-b1bf-2356fb992a7c
ms.date: 12/05/2018
ms.keywords: IProvideClassInfo, IProvideClassInfo interface [COM], IProvideClassInfo interface [COM],described, _com_iprovideclassinfo, com.iprovideclassinfo, ocidl/IProvideClassInfo
ms.topic: interface
f1_keywords:
- ocidl/IProvideClassInfo
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
- IProvideClassInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProvideClassInfo interface


## -description


Provides access to the type information for an object's coclass entry in its type library.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideClassInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProvideClassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProvideClassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iprovideclassinfo-getclassinfo">GetClassInfo</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> interface for the object's type information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/">coclass</a>
 

 

