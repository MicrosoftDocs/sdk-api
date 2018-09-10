---
UID: NN:sbtsv.ITsSbGenericNotifySink
title: ITsSbGenericNotifySink
author: windows-sdk-content
description: Exposes methods that reports completion to and gets wait time from the Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbgenericnotifysink.htm
tech.root: termserv
ms.assetid: 03a895ef-6c67-4537-bc1c-838b65ae3487
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITsSbGenericNotifySink, ITsSbGenericNotifySink interface [Remote Desktop Services], ITsSbGenericNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbGenericNotifySink, termserv.itssbgenericnotifysink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SbTsV.idl
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
 - sbtsv.h
api_name:
 - ITsSbGenericNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbGenericNotifySink interface


## -description


Exposes methods that reports completion to and gets wait time from the Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbGenericNotifySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbGenericNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbGenericNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/685471bd-3228-4fdd-a91f-e8da2a6c3b91">GetWaitTimeout</a>
</td>
<td align="left" width="63%">
Retrieves the wait timeout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d8dd044-988e-4e37-9936-2a3639dedca1">OnCompleted</a>
</td>
<td align="left" width="63%">
Reports completion to RD Connection Broker. 

</td>
</tr>
</table> 

