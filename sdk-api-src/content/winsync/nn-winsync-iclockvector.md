---
UID: NN:winsync.IClockVector
title: IClockVector
author: windows-sdk-content
description: Represents a clock vector in a knowledge structure.
old-location: winsync\iclockvector.htm
tech.root: winsync
ms.assetid: 31aef38d-a6df-4645-a192-9145d3ec90ad
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IClockVector, IClockVector interface [Windows Sync], IClockVector interface [Windows Sync],described, winsync.iclockvector, winsync/IClockVector
ms.prod: windows
ms.technology: windows-sdk
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
 - IClockVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IClockVector interface


## -description


Represents a clock vector in a knowledge structure.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClockVector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IClockVector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClockVector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15ce120e-dabc-4827-b317-82784466c1f1">GetClockVectorElementCount</a>
</td>
<td align="left" width="63%">
Gets the number of elements that are contained in the clock vector.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0712a2b-5aeb-458d-bc0f-c18eeb7ba9ff">GetClockVectorElements</a>
</td>
<td align="left" width="63%">
Returns an enumerator that iterates through the clock vector elements.


</td>
</tr>
</table> 


## -remarks



A clock vector defines the changes that are contained in a knowledge structure by using a list of <b>IClockVectorElement</b> objects. An <b>IClockVectorElement</b> object exists for each replica that has made a change that is contained in the knowledge. A change that is made by a particular replica is defined to be contained in the knowledge when the tick count for the change occurs between zero and the tick count contained in <b>IClockVectorElement</b> that tracks that replica.





## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

