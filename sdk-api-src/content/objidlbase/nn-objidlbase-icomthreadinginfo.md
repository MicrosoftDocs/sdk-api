---
UID: NN:objidlbase.IComThreadingInfo
title: IComThreadingInfo (objidlbase.h)
author: windows-sdk-content
description: Enables you to obtain the following information about the apartment and thread that the caller is executing in:\_apartment type, thread type, and thread GUID. It also allows you to specify a thread GUID.
old-location: com\icomthreadinginfo.htm
tech.root: com
ms.assetid: fa4c7d82-ec5d-43d6-914e-bba60ad19aa2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComThreadingInfo, IComThreadingInfo interface [COM], IComThreadingInfo interface [COM],described, _com_icomthreadinginfo_interface, com.icomthreadinginfo, objidlbase/IComThreadingInfo
ms.topic: interface
f1_keywords: ["objidlbase/IComThreadingInfo"]
req.header: objidlbase.h
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
 - IComThreadingInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComThreadingInfo interface


## -description


Enables you to obtain the following information about the apartment and thread that the caller is executing in: apartment type, thread type, and thread GUID. It also allows you to specify a thread GUID.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComThreadingInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComThreadingInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComThreadingInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentapartmenttype">GetCurrentApartmentType</a>
</td>
<td align="left" width="63%">
Retrieves the type of apartment in which the caller is executing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentlogicalthreadid">GetCurrentLogicalThreadId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the thread in which the caller is executing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentthreadtype">GetCurrentThreadType</a>
</td>
<td align="left" width="63%">
Retrieves the type of thread in which the caller is executing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-setcurrentlogicalthreadid">SetCurrentLogicalThreadId</a>
</td>
<td align="left" width="63%">
Sets the GUID of the thread in which the caller is executing.

</td>
</tr>
</table> 


## -remarks



 An instance of this interface for the current context can be obtained using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>.



