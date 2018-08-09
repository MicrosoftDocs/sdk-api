---
UID: NN:tpmvscmgr.ITpmVirtualSmartCardManagerStatusCallback
title: ITpmVirtualSmartCardManagerStatusCallback
author: windows-sdk-content
description: Notifies the caller of the progress of the requested operation or any resulting errors.
old-location: security\itpmvirtualsmartcardmanagerstatuscallback.htm
old-project: secauthn
ms.assetid: 6CB62E42-16FD-453F-9566-B4DFCDAC7368
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITpmVirtualSmartCardManagerStatusCallback, ITpmVirtualSmartCardManagerStatusCallback interface [Security], ITpmVirtualSmartCardManagerStatusCallback interface [Security],described, security.itpmvirtualsmartcardmanagerstatuscallback, tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
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
product: Windows
targetos: Windows
req.lib: Vscmgr.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITpmVirtualSmartCardManagerStatusCallback interface


## -description


Notifies the caller of the progress of the requested operation or any resulting errors.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITpmVirtualSmartCardManagerStatusCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITpmVirtualSmartCardManagerStatusCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/936F22EA-1C9F-4328-B71F-FA7720396F6F">ReportError</a>
</td>
<td align="left" width="63%">
Reports any errors from the requested operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E20CF68F-0DFB-48E4-9B68-83A8E8763424">ReportProgress</a>
</td>
<td align="left" width="63%">
Reports the progress of the current operation.

</td>
</tr>
</table> 

