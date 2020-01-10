---
UID: NN:shobjidl_core.IObjectWithProgID
title: IObjectWithProgID (shobjidl_core.h)
description: Exposes methods that provide access to the ProgID associated with an object.
old-location: shell\IObjectWithProgID.htm
tech.root: shell
ms.assetid: 3b66ba49-ed39-464e-b15a-c72fdff7f5e5
ms.date: 12/05/2018
ms.keywords: IObjectWithProgID, IObjectWithProgID interface [Windows Shell], IObjectWithProgID interface [Windows Shell],described, _shell_IObjectWithProgID, shell.IObjectWithProgID, shobjidl_core/IObjectWithProgID
f1_keywords:
- shobjidl_core/IObjectWithProgID
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- shobjidl_core.h
api_name:
- IObjectWithProgID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectWithProgID interface


## -description


Exposes methods that provide access to the ProgID associated with an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithProgID</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectWithProgID</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithProgID</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithprogid-getprogid">GetProgID</a>
</td>
<td align="left" width="63%">
Retrieves the ProgID associated with an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithprogid-setprogid">SetProgID</a>
</td>
<td align="left" width="63%">
Sets the ProgID of an object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/fa-progids">Programmatic Identifiers</a>
 

 

