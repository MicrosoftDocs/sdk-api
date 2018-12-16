---
UID: NN:oaidl.IDispatch
title: IDispatch
author: windows-sdk-content
description: Exposes objects, methods and properties to programming tools and other applications that support Automation.
old-location: automat\idispatch.htm
tech.root: automat
ms.assetid: ebbff4bc-36b2-4861-9efa-ffa45e013eb5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDispatch, IDispatch interface [Automation], IDispatch interface [Automation],described, _oa96_IDispatch_Interface, automat.idispatch, oaidl/IDispatch
ms.topic: interface
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - oaidl.h
api_name:
 - IDispatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDispatch interface


## -description


Exposes objects, methods and properties to programming tools and other applications that support Automation. COM components implement the <b>IDispatch</b> interface to enable access by Automation clients, such as Visual Basic. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDispatch</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDispatch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDispatch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f6cf233-3481-436e-8d6a-51f93bf91619">GetIDsOfNames</a>
</td>
<td align="left" width="63%">
Maps a single member and an optional set of argument names to a corresponding set of integer DISPIDs, which can be used on subsequent calls to <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">Invoke</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc1ec9aa-6c40-4e70-819c-a7c6dd6b8c99">GetTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the type information for an object, which can then be used to get the type information for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da876d53-cb8a-465c-a43e-c0eb272e2a12">GetTypeInfoCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of type information interfaces that an object provides (either 0 or 1).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">Invoke</a>
</td>
<td align="left" width="63%">
Provides access to properties and methods exposed by an object.

</td>
</tr>
</table> 

