---
UID: NN:winsync.IRangeException
title: IRangeException
author: windows-sdk-content
description: Represents an item ID range to exclude from a knowledge object.
old-location: winsync\irangeexception.htm
tech.root: winsync
ms.assetid: 7eea9fe0-80e7-43a9-a797-df12d4d809dc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IRangeException, IRangeException interface [Windows Sync], IRangeException interface [Windows Sync],described, winsync.irangeexception, winsync/IRangeException
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - winsync.h
api_name:
 - IRangeException
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRangeException interface


## -description


Represents an item ID range to exclude from a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRangeException</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRangeException</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRangeException</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a13bb4c-ed0e-45f0-a78f-13eadd32760e">GetClockVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with this exception.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1725d0b8-2ecb-4cce-b20f-7e8d0da502de">GetClosedRangeEnd</a>
</td>
<td align="left" width="63%">
Gets the upper bound of the range of item IDs to exclude.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c3c4e92-8c0d-4a3d-97be-029d2c386af4">GetClosedRangeStart</a>
</td>
<td align="left" width="63%">
Gets the lower bound of the range of item IDs to exclude.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

