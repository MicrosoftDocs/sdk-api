---
UID: NN:comsvcs.IContextState
title: IContextState
author: windows-sdk-content
description: Controls object deactivation and transaction voting by manipulating context state flags.
old-location: cos\icontextstate.htm
tech.root: cossdk
ms.assetid: cba54ad7-c670-4efb-ad3b-aca1daabc4a3
ms.author: windowssdkdev
ms.date: 08/31/2018
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IContextState interface


## -description


Controls object deactivation and transaction voting by manipulating context state flags. By calling the methods of this interface, you can set consistent and done flags independently of each other and get the current status of each flag. Also, the methods of this interface return errors that indicate the absence of just-in-time (JIT) activation or the absence of a transaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextState</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IContextState</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms681258(v=VS.85).aspx">GetDeactivateOnReturn</a>
</td>
<td align="left" width="63%">
Retrieves the value of the done flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682775(v=VS.85).aspx">GetMyTransactionVote</a>
</td>
<td align="left" width="63%">
Retrieves the value of the consistent flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679511(v=VS.85).aspx">SetDeactivateOnReturn</a>
</td>
<td align="left" width="63%">
Sets the done flag, which controls whether the object deactivates on method return.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687722(v=VS.85).aspx">SetMyTransactionVote</a>
</td>
<td align="left" width="63%">
Sets the consistent flag.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685142(v=VS.85).aspx">Consistent and Done Flags</a>
 

 

