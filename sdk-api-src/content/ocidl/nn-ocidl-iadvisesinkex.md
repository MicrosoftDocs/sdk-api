---
UID: NN:ocidl.IAdviseSinkEx
title: IAdviseSinkEx
author: windows-sdk-content
description: This interface is derived from IAdviseSink to provide extensions for notifying the sink of changes in an object's view status.
old-location: com\iadvisesinkex.htm
old-project: com
ms.assetid: d1a52353-dd86-4083-9dbc-3a6f363a1a57
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAdviseSinkEx, IAdviseSinkEx interface [COM], IAdviseSinkEx interface [COM],described, _ole_iadvisesinkex, com.iadvisesinkex, ocidl/IAdviseSinkEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IAdviseSinkEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAdviseSinkEx interface


## -description


This interface is derived from <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> to provide extensions for notifying the sink of changes in an object's view status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAdviseSinkEx</b> interface inherits from <b>IAdviseSink</b>. <b>IAdviseSinkEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAdviseSinkEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d5129aa-341c-4c69-8c0c-b7c3e62a57c1">OnViewStatusChange</a>
</td>
<td align="left" width="63%">
Notifies the sink that a view status of an object has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>
 

 

