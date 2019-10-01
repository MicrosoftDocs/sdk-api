---
UID: NN:ocidl.IPersistStreamInit
title: IPersistStreamInit (ocidl.h)
author: windows-sdk-content
description: A replacement for IPersistStream that adds an initialization method.
old-location: com\ipersiststreaminit.htm
tech.root: com
ms.assetid: 49c413b3-3523-4602-9ec1-19f4e0fe5651
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersistStreamInit, IPersistStreamInit interface [COM], IPersistStreamInit interface [COM],described, _com_ipersiststreaminit, com.ipersiststreaminit, ocidl/IPersistStreamInit
ms.topic: interface
f1_keywords: 
 - "ocidl/IPersistStreamInit"
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
 - IPersistStreamInit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistStreamInit interface


## -description


A replacement for <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> that adds an initialization method.

This interface is not derived from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>; it is mutually exclusive with <b>IPersistStream</b>. An object chooses to support only one of the two interfaces, based on whether it requires the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew">InitNew</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistStreamInit</b> interface inherits from <b>IPersist</b>. <b>IPersistStreamInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistStreamInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-getsizemax">GetSizeMax</a>
</td>
<td align="left" width="63%">
Retrieves the size of the stream needed to save the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew">InitNew</a>
</td>
<td align="left" width="63%">
Initializes an object to a default state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-isdirty">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-load">Load</a>
</td>
<td align="left" width="63%">
Initializes an object from the stream where it was saved previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-save">Save</a>
</td>
<td align="left" width="63%">
Saves an object to the specified stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>
 

 

