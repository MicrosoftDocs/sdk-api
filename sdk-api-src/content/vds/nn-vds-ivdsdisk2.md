---
UID: NN:vds.IVdsDisk2
title: IVdsDisk2
author: windows-sdk-content
description: Provides a method to set the SAN mode of a disk to offline or online.
old-location: base\ivdsdisk2.htm
tech.root: VDS
ms.assetid: 9fb8a08e-412d-415a-aa27-cc0180599903
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVdsDisk2, IVdsDisk2 interface, IVdsDisk2 interface,described, base.ivdsdisk2, vds/IVdsDisk2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsDisk2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsDisk2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to set the SAN mode of a disk to offline  or online.<div class="alert"><b>Note</b>  Starting with Windows Vista with Service Pack 1 (SP1), this interface is supserseded by the <a href="https://msdn.microsoft.com/f30ceaa0-ff4b-49fb-b140-b6725810cd06">IVdsDiskOnline</a> interface.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDisk2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsDisk2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDisk2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17bdb6f4-7d85-4aa6-b89b-a752332cc224">SetSANMode</a>
</td>
<td align="left" width="63%">
Sets the SAN mode of a disk to offline or online.

</td>
</tr>
</table> 

