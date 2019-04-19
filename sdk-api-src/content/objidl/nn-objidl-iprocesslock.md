---
UID: NN:objidl.IProcessLock
title: IProcessLock (objidl.h)
author: windows-sdk-content
description: Used by ISurrogateService to prevent the process from terminating due to a time-out.
old-location: com\iprocesslock.htm
tech.root: com
ms.assetid: 49ec5657-d54e-4af7-8c20-00de383ecf89
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProcessLock, IProcessLock interface [COM], IProcessLock interface [COM],described, _com_iprocesslock, com.iprocesslock, objidl/IProcessLock
ms.topic: interface
req.header: objidl.h
req.include-header: 
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
 - ObjIdl.h
api_name:
 - IProcessLock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProcessLock interface


## -description


<p class="CCE_Message">[The use of this interface is not recommended; use the <a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a> interface instead.]

Used by <a href="https://msdn.microsoft.com/01773aa6-3eb5-43dd-8a10-d1351a07fe1f">ISurrogateService</a> to prevent the process from terminating due to a time-out.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProcessLock</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IProcessLock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProcessLock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c82273f-7303-45c2-92e2-48ffab094756">AddRefOnProcess</a>
</td>
<td align="left" width="63%">
Increments the reference count of the process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0943afc-b20f-4082-b561-552370a630a1">ReleaseRefOnProcess</a>
</td>
<td align="left" width="63%">
Decrements the reference count of the process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a>
 

 

