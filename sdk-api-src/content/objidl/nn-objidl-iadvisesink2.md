---
UID: NN:objidl.IAdviseSink2
title: IAdviseSink2
author: windows-sdk-content
description: The IAdviseSink2 interface is an extension of the IAdviseSink interface, adding the method OnLinkSrcChange to the contract to handle a change in the moniker of a linked object.
old-location: com\iadvisesink2.htm
tech.root: com
ms.assetid: 80f55377-8a1e-42b1-8fe0-5896620c8062
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAdviseSink2, IAdviseSink2 interface [COM], IAdviseSink2 interface [COM],described, _ole_iadvisesink2, com.iadvisesink2, objidl/IAdviseSink2
ms.prod: windows
ms.technology: windows-sdk
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
 - IAdviseSink2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAdviseSink2 interface


## -description


The <b>IAdviseSink2</b> interface is an extension of the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface, adding the method <a href="https://msdn.microsoft.com/753ac9a3-0207-4c98-9d86-5ac16be2c5fa">OnLinkSrcChange</a> to the contract to handle a change in the moniker of a linked object. This avoids overloading the implementation <a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">IAdviseSink::OnRename</a> to handle the renaming of both embedded objects and linked objects. In applications where different blocks of code might execute depending on which of these two similar events has occurred, using the same method for both events complicates testing and debugging.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAdviseSink2</b> interface inherits from <b>IAdviseSink</b>. <b>IAdviseSink2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAdviseSink2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/753ac9a3-0207-4c98-9d86-5ac16be2c5fa">OnLinkSrcChange</a>
</td>
<td align="left" width="63%">
Advises that link source has changed.

</td>
</tr>
</table> 

