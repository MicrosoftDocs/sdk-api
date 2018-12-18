---
UID: NN:windows.foundation.IAsyncAction
title: IAsyncAction
author: windows-sdk-content
description: Represents an asynchronous action.
old-location: winrt\iasyncaction.htm
tech.root: WinRT
ms.assetid: E5D567F6-FFDE-4E51-8D52-638D30252549
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAsyncAction, IAsyncAction interface [Windows Runtime], IAsyncAction interface [Windows Runtime],described, windows/IAsyncAction, winrt.iasyncaction
ms.topic: interface
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
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
 - Windows.Foundation.h
api_name:
 - IAsyncAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsyncAction interface


## -description


Represents an asynchronous action.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsyncAction</b> interface inherits from <b>IInspectable</b>. <b>IAsyncAction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAsyncAction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5050BF84-F9E0-4B3E-9252-6C5C1060826E">get_Completed</a>
</td>
<td align="left" width="63%">
Gets the method that is called when the asynchronous action completes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0">GetResults</a>
</td>
<td align="left" width="63%">
Gets the outcome of an asynchronous action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/632800E4-D02B-4D45-8A9B-B373AC938558">put_Completed</a>
</td>
<td align="left" width="63%">
Sets the method that is called when the asynchronous action completes. 

</td>
</tr>
</table> 


## -remarks



The <b>IAsyncAction</b> interface represents an asynchronous action that does not return a result and does not have progress notifications.  When the action completes, the <a href="https://msdn.microsoft.com/B410E7C1-B108-4204-9AD1-663F7E05BBC3">AsyncActionCompletedHandler</a> specified by <a href="https://msdn.microsoft.com/5050BF84-F9E0-4B3E-9252-6C5C1060826E">get_Completed</a>  is invoked, and this is the only result from the action.



