---
UID: NN:winsync.IClockVectorElement
title: IClockVectorElement
author: windows-sdk-content
description: Represents a clock vector element of a knowledge structure.
old-location: winsync\iclockvectorelement.htm
tech.root: winsync
ms.assetid: cae24ef0-5b31-48c2-99bd-9e0954ec3b37
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IClockVectorElement, IClockVectorElement interface [Windows Sync], IClockVectorElement interface [Windows Sync],described, winsync.iclockvectorelement, winsync/IClockVectorElement
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
 - IClockVectorElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IClockVectorElement interface


## -description


Represents a clock vector element of a knowledge structure.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClockVectorElement</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IClockVectorElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClockVectorElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6f1ce72-e8fd-4f87-a184-7126e880804d">GetReplicaKey</a>
</td>
<td align="left" width="63%">
Gets the replica key for the replica that is associated with this clock vector element.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/927d769b-c100-4f5f-a243-c5ca53b4d528">GetTickCount</a>
</td>
<td align="left" width="63%">
Gets the tick count that defines the upper bound on the range of tick counts that are contained in this clock vector element.


</td>
</tr>
</table> 


## -remarks



The clock vector elements of a clock vector represent the changes that are contained in a knowledge structure. A change that is made by a particular replica is defined to be contained in the knowledge when the tick count for the change occurs between zero and the tick count contained in the <b>IClockVectorElement</b> that tracks that replica.




## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

