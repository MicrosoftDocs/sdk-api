---
UID: NN:mbnapi.IMbnConnectionContext
title: IMbnConnectionContext
author: windows-sdk-content
description: Manages connection contexts.
old-location: mbn\imbnconnectioncontext.htm
old-project: mbn
ms.assetid: a9bc52dc-47f9-4b20-b98d-0287464a89e5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnConnectionContext, IMbnConnectionContext interface [Microsoft Broadband Networks], IMbnConnectionContext interface [Microsoft Broadband Networks],described, mbn.imbnconnectioncontext, mbnapi/IMbnConnectionContext
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionContext interface


## -description


Manages connection contexts.

A connection context is an abstraction of a specific set of network configuration parameters for setting up a virtual circuit or flow on top of the physical Mobile Broadband connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnectionContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eceba2a8-baff-436f-b561-d9e130df5702">GetProvisionedContexts</a>
</td>
<td align="left" width="63%">
Gets a list of connection contexts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/738a3037-01a9-465a-a67d-979a29968b68">SetProvisionedContext</a>
</td>
<td align="left" width="63%">
Adds or updates a provisioned context.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.



