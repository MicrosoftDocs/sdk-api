---
UID: NN:oaidl.IDispatch
title: IDispatch (oaidl.h)
author: windows-sdk-content
description: Exposes objects, methods and properties to programming tools and other applications that support Automation.
old-location: automat\idispatch.htm
tech.root: automat
ms.assetid: ebbff4bc-36b2-4861-9efa-ffa45e013eb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDispatch, IDispatch interface [Automation], IDispatch interface [Automation],described, _oa96_IDispatch_Interface, automat.idispatch, oaidl/IDispatch
ms.topic: interface
f1_keywords: 
 - "oaidl/IDispatch"
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
ms.custom: 19H1
---

# IDispatch interface


## -description


Exposes objects, methods and properties to programming tools and other applications that support Automation. COM components implement the <b>IDispatch</b> interface to enable access by Automation clients, such as Visual Basic. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDispatch</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDispatch</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames">GetIDsOfNames</a>
</td>
<td align="left" width="63%">
Maps a single member and an optional set of argument names to a corresponding set of integer DISPIDs, which can be used on subsequent calls to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo">GetTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the type information for an object, which can then be used to get the type information for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount">GetTypeInfoCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of type information interfaces that an object provides (either 0 or 1).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Provides access to properties and methods exposed by an object.

</td>
</tr>
</table> 

