---
UID: NN:mfobjects.IMFAsyncCallbackLogging
title: IMFAsyncCallbackLogging
author: windows-sdk-content
description: Provides logging information about the parent object the async callback is associated with.
old-location: mf\imfasynccallbacklogging.htm
tech.root: medfound
ms.assetid: 8b4de920-8e82-4e50-b801-82842da8a6ae
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFAsyncCallbackLogging, IMFAsyncCallbackLogging interface [Media Foundation], IMFAsyncCallbackLogging interface [Media Foundation],described, mf.imfasynccallbacklogging, mfobjects/IMFAsyncCallbackLogging
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - Mfobjects.h
api_name:
 - IMFAsyncCallbackLogging
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAsyncCallbackLogging interface


## -description


Provides logging information about the parent object the async callback is associated with.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAsyncCallbackLogging</b> interface inherits from <b>IMFAsyncCallback</b>. <b>IMFAsyncCallbackLogging</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAsyncCallbackLogging</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2628b3f-37b7-4317-960e-cbd2339aade6">GetObjectPointer</a>
</td>
<td align="left" width="63%">
Gets the pointer to the parent object the async callback is associated with. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f556a163-54d1-4353-ab9e-e8aa6bf35958">GetObjectTag</a>
</td>
<td align="left" width="63%">
Gets the tag of the parent object the async callback is associated object.

</td>
</tr>
</table> 


## -remarks



<b>IMFAsyncCallbackLogging</b> is primarily used for async callbacks to return an ID of the parent object that they are associated with.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

