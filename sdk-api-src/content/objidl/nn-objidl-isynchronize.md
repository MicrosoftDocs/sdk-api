---
UID: NN:objidl.ISynchronize
title: ISynchronize
author: windows-sdk-content
description: Provides asynchronous communication between objects about the occurrence of an event.
old-location: com\isynchronize.htm
tech.root: com
ms.assetid: 2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ISynchronize, ISynchronize interface [COM], ISynchronize interface [COM],described, _com_isynchronize, com.isynchronize, objidlbase/ISynchronize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: ObjIdl.h
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
 - objidlbase.h
api_name:
 - ISynchronize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISynchronize interface


## -description


Provides asynchronous communication between objects about the occurrence of an event. Objects that implement <b>ISynchronize</b> can receive indications that an event has occurred, and they can respond to queries about the event. In this way, clients can make sure that one request has been processed before they submit a subsequent request that depends on completion of the first one.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronize</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ISynchronize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33c56a33-9954-4612-ba0f-396ccdc48bf3">Reset</a>
</td>
<td align="left" width="63%">
Sets the synchronization object to the nonsignaled state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c55b9ffc-2e28-427b-8c77-349f554469e5">Signal</a>
</td>
<td align="left" width="63%">
Sets the synchronization object to the signaled state and causes pending wait operations to return S_OK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1abed0be-b4e3-41f4-af6c-e327ce934b59">Wait</a>
</td>
<td align="left" width="63%">
Waits for the synchronization object to be signaled or for a specified timeout period to elapse, whichever comes first.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6a5be504-b5fa-491c-ba65-74c5de39e263">ISynchronizeContainer</a>
 

 

