---
UID: NN:rtscom.IRealTimeStylusSynchronization
title: IRealTimeStylusSynchronization
author: windows-sdk-content
description: Synchronizes access to the RealTimeStylus Class object.
old-location: tablet\irealtimestylussynchronization.htm
tech.root: tablet
ms.assetid: fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IRealTimeStylusSynchronization, IRealTimeStylusSynchronization interface [Tablet PC], IRealTimeStylusSynchronization interface [Tablet PC],described, fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd, rtscom/IRealTimeStylusSynchronization, tablet.irealtimestylussynchronization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylusSynchronization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRealTimeStylusSynchronization interface


## -description



Synchronizes access to the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRealTimeStylusSynchronization</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRealTimeStylusSynchronization</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRealTimeStylusSynchronization</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74e315c5-99c2-4ba5-bca5-72d812624fa0">AcquireLock</a>
</td>
<td align="left" width="63%">
Retrieves the specified lock to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13970fda-7b2a-4fb7-9403-8d9aad39d83a">ReleaseLock</a>
</td>
<td align="left" width="63%">
Releases the specified lock.

</td>
</tr>
</table> 


## -remarks



Use locks when you must protect access to and modification of the plug-ins or properties of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object through the <b>IRealTimeStylusSynchronization Interface</b> interface.

Use the <a href="https://msdn.microsoft.com/d472b588-b208-4665-9364-f2c92fe09bcd">RealTimeStylusLockType Enumeration</a> enumeration to specify the lock.




## -see-also




<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>
 

 

