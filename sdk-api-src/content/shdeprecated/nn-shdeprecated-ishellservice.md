---
UID: NN:shdeprecated.IShellService
title: IShellService (shdeprecated.h)
description: Deprecated. IShellService Exposes one method that declares ownership when a service component implementing a certain interface is shared among multiple clients, such as Windows Internet Explorer and Windows Explorer.helpviewer_keywords: ["IShellService","IShellService interface [Windows Shell]","IShellService interface [Windows Shell]","described","shdeprecated/IShellService","shell.IShellService","zone_IShellService"]
old-location: shell\IShellService.htm
tech.root: shell
ms.assetid: 0b845907-a879-4f87-a6f5-8cc86dfe03ff
ms.date: 12/05/2018
ms.keywords: IShellService, IShellService interface [Windows Shell], IShellService interface [Windows Shell],described, shdeprecated/IShellService, shell.IShellService, zone_IShellService
f1_keywords:
- shdeprecated/IShellService
dev_langs:
- c++
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
- Shdeprecated.h
api_name:
- IShellService
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# IShellService interface


## -description


Deprecated. <b>IShellService</b> Exposes one method that declares ownership when a service component implementing a certain interface is shared among multiple clients, such as Windows Internet Explorer and Windows Explorer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ishellservice-setowner">SetOwner</a>
</td>
<td align="left" width="63%">
Deprecated. Declares an owner reference to the service object.

</td>
</tr>
</table> 

