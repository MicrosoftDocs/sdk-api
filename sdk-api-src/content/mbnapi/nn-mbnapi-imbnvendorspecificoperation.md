---
UID: NN:mbnapi.IMbnVendorSpecificOperation
title: IMbnVendorSpecificOperation
author: windows-sdk-content
description: Interface to pass requests from an application to the underlying Mobile Broadband miniport drivers.
old-location: mbn\imbnvendorspecificoperation.htm
tech.root: mbn
ms.assetid: cbc905f6-c5ac-4c6a-9021-4ec00b938bb2
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMbnVendorSpecificOperation, IMbnVendorSpecificOperation interface [Microsoft Broadband Networks], IMbnVendorSpecificOperation interface [Microsoft Broadband Networks],described, mbn.imbnvendorspecificoperation, mbnapi/IMbnVendorSpecificOperation
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnVendorSpecificOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnVendorSpecificOperation interface


## -description


Interface to pass requests from an application to the underlying Mobile Broadband miniport drivers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnVendorSpecificOperation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnVendorSpecificOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnVendorSpecificOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adae9d6c-3fd4-42f6-8f6a-0047f3e0aad0">SetVendorSpecific</a>
</td>
<td align="left" width="63%">
Send a request to the miniport driver.

</td>
</tr>
</table> 


## -remarks



The calling application can acquire this interface by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.



