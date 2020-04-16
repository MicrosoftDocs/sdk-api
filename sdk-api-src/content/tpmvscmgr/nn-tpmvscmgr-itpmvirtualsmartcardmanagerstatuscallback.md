---
UID: NN:tpmvscmgr.ITpmVirtualSmartCardManagerStatusCallback
title: ITpmVirtualSmartCardManagerStatusCallback (tpmvscmgr.h)
description: Notifies the caller of the progress of the requested operation or any resulting errors.helpviewer_keywords: ["ITpmVirtualSmartCardManagerStatusCallback","ITpmVirtualSmartCardManagerStatusCallback interface [Security]","ITpmVirtualSmartCardManagerStatusCallback interface [Security]","described","security.itpmvirtualsmartcardmanagerstatuscallback","tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback"]
old-location: security\itpmvirtualsmartcardmanagerstatuscallback.htm
tech.root: SecAuthN
ms.assetid: 6CB62E42-16FD-453F-9566-B4DFCDAC7368
ms.date: 12/05/2018
ms.keywords: ITpmVirtualSmartCardManagerStatusCallback, ITpmVirtualSmartCardManagerStatusCallback interface [Security], ITpmVirtualSmartCardManagerStatusCallback interface [Security],described, security.itpmvirtualsmartcardmanagerstatuscallback, tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback
f1_keywords:
- tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback
dev_langs:
- c++
req.header: tpmvscmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tpmvscmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vscmgr.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Vscmgr.lib
- Vscmgr.dll
api_name:
- ITpmVirtualSmartCardManagerStatusCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITpmVirtualSmartCardManagerStatusCallback interface


## -description


Notifies the caller of the progress of the requested operation or any resulting errors.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITpmVirtualSmartCardManagerStatusCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITpmVirtualSmartCardManagerStatusCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITpmVirtualSmartCardManagerStatusCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tpmvscmgr/nf-tpmvscmgr-itpmvirtualsmartcardmanagerstatuscallback-reporterror">ReportError</a>
</td>
<td align="left" width="63%">
Reports any errors from the requested operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tpmvscmgr/nf-tpmvscmgr-itpmvirtualsmartcardmanagerstatuscallback-reportprogress">ReportProgress</a>
</td>
<td align="left" width="63%">
Reports the progress of the current operation.

</td>
</tr>
</table> 

