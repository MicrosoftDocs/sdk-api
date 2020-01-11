---
UID: NN:shobjidl.IEnumReadyCallback
title: IEnumReadyCallback (shobjidl.h)
description: Exposes methods that enable the view to notify the implementer when the enumeration has completed.
old-location: shell\IEnumReadyCallback.htm
tech.root: shell
ms.assetid: 6c36e13d-9bd8-4ec1-980a-dc4ebd4dbcd9
ms.date: 12/05/2018
ms.keywords: IEnumReadyCallback, IEnumReadyCallback interface [Windows Shell], IEnumReadyCallback interface [Windows Shell],described, _shell_IEnumReadyCallback, shell.IEnumReadyCallback, shobjidl/IEnumReadyCallback
f1_keywords:
- shobjidl/IEnumReadyCallback
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Shobjidl.h
api_name:
- IEnumReadyCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumReadyCallback interface


## -description


Exposes methods that enable the view to notify the implementer when the enumeration has completed.  The view calls this method to tell the implementer that the enumeration can be retrieved via <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents">IEnumerableView::CreateEnumIDListFromContents</a>.  The callback allows the implementer to share the views enumeration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumReadyCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumReadyCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumReadyCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ienumreadycallback-enumready">EnumReady</a>
</td>
<td align="left" width="63%">
Notifies the implementer that the view's item enumeration has completed.  This callback interface is provided to the view via <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ienumerableview-setenumreadycallback">IEnumerableView::SetEnumReadyCallback</a>


</td>
</tr>
</table> 

