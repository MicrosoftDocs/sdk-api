---
UID: NN:comsvcs.IContextState
title: IContextState
author: windows-sdk-content
description: Controls object deactivation and transaction voting by manipulating context state flags.
old-location: cos\icontextstate.htm
old-project: cossdk
ms.assetid: cba54ad7-c670-4efb-ad3b-aca1daabc4a3
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IContextState, IContextState interface [COM+], IContextState interface [COM+],described, _cos_IContextState, comsvcs/IContextState, cos.icontextstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IContextState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IContextState interface


## -description


Controls object deactivation and transaction voting by manipulating context state flags. By calling the methods of this interface, you can set consistent and done flags independently of each other and get the current status of each flag. Also, the methods of this interface return errors that indicate the absence of just-in-time (JIT) activation or the absence of a transaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextState</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContextState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e9623eb-1bf1-4649-9071-b731bf95a401">GetDeactivateOnReturn</a>
</td>
<td align="left" width="63%">
Retrieves the value of the done flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72384c53-ce4a-413e-8ff6-33925c8cd0df">GetMyTransactionVote</a>
</td>
<td align="left" width="63%">
Retrieves the value of the consistent flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29dfeb6f-1961-4d6f-b5c4-fcd0eb4a7bec">SetDeactivateOnReturn</a>
</td>
<td align="left" width="63%">
Sets the done flag, which controls whether the object deactivates on method return.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec88f99a-cb24-42a9-8f2a-add7ddbec719">SetMyTransactionVote</a>
</td>
<td align="left" width="63%">
Sets the consistent flag.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a641fa95-5587-4362-9869-e5c27c6dd2ce">Consistent and Done Flags</a>
 

 

