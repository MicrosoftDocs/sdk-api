---
UID: NN:objidl.IForegroundTransfer
title: IForegroundTransfer (objidl.h)
description: Transfers the foreground window to the process hosting the COM server.
helpviewer_keywords: ["IForegroundTransfer","IForegroundTransfer interface [COM]","IForegroundTransfer interface [COM]","described","_com_iforegroundtransfer","com.iforegroundtransfer","objidl/IForegroundTransfer"]
old-location: com\iforegroundtransfer.htm
tech.root: com
ms.assetid: 21857592-0f98-4eb4-a153-4ce20edf26c7
ms.date: 12/05/2018
ms.keywords: IForegroundTransfer, IForegroundTransfer interface [COM], IForegroundTransfer interface [COM],described, _com_iforegroundtransfer, com.iforegroundtransfer, objidl/IForegroundTransfer
f1_keywords:
- objidl/IForegroundTransfer
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
- ObjIdl.h
api_name:
- IForegroundTransfer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IForegroundTransfer interface


## -description


Transfers the foreground window to the process hosting the COM server. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IForegroundTransfer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IForegroundTransfer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IForegroundTransfer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iforegroundtransfer-allowforegroundtransfer">AllowForegroundTransfer</a>
</td>
<td align="left" width="63%">
Yields the foreground window to the COM server process.

</td>
</tr>
</table> 

