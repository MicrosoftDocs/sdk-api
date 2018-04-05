---
UID: NN:mbnapi.IMbnServiceActivation
title: IMbnServiceActivation
author: windows-driver-content
description: Pass-through mechanism for cellular service activation.
old-location: mbn\imbnserviceactivation.htm
old-project: mbn
ms.assetid: cf23be24-f7a8-41b9-81f1-c267a265f85b
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnServiceActivation, IMbnServiceActivation interface [Microsoft Broadband Networks], IMbnServiceActivation interface [Microsoft Broadband Networks], described, mbn.imbnserviceactivation, mbnapi/IMbnServiceActivation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnServiceActivation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnServiceActivation interface


## -description


Pass-through mechanism for cellular service activation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnServiceActivation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnServiceActivation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnServiceActivation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c131363-9403-4c7a-984d-6602b879c08e">Activate</a>
</td>
<td align="left" width="63%">
Sends the service activation request to the network.

</td>
</tr>
</table> 


## -remarks



An <b>IMbnServiceActivation</b> interface can be obtained by calling <b>QueryInterface</b>  from <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.



