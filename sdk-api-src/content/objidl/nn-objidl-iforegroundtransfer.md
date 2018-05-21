---
UID: NN:objidl.IForegroundTransfer
title: IForegroundTransfer
author: windows-driver-content
description: Transfers the foreground window to the process hosting the COM server.
old-location: com\iforegroundtransfer.htm
old-project: com
ms.assetid: 21857592-0f98-4eb4-a153-4ce20edf26c7
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IForegroundTransfer, IForegroundTransfer interface [COM], IForegroundTransfer interface [COM],described, _com_iforegroundtransfer, com.iforegroundtransfer, objidl/IForegroundTransfer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IForegroundTransfer
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IForegroundTransfer interface


## -description


Transfers the foreground window to the process hosting the COM server. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IForegroundTransfer</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IForegroundTransfer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/54d138f5-5f16-4eb8-bbac-2d057b7dab2f">AllowForegroundTransfer</a>
</td>
<td align="left" width="63%">
Yields the foreground window to the COM server process.

</td>
</tr>
</table> 

