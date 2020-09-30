---
UID: NN:sbtsv.ITsSbGenericNotifySink
title: ITsSbGenericNotifySink (sbtsv.h)
description: Exposes methods that reports completion to and gets wait time from the Remote Desktop Connection Broker (RD Connection Broker).
helpviewer_keywords: ["ITsSbGenericNotifySink","ITsSbGenericNotifySink interface [Remote Desktop Services]","ITsSbGenericNotifySink interface [Remote Desktop Services]","described","sbtsv/ITsSbGenericNotifySink","termserv.itssbgenericnotifysink"]
old-location: termserv\itssbgenericnotifysink.htm
tech.root: TermServ
ms.assetid: 03a895ef-6c67-4537-bc1c-838b65ae3487
ms.date: 12/05/2018
ms.keywords: ITsSbGenericNotifySink, ITsSbGenericNotifySink interface [Remote Desktop Services], ITsSbGenericNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbGenericNotifySink, termserv.itssbgenericnotifysink
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbGenericNotifySink
 - sbtsv/ITsSbGenericNotifySink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGenericNotifySink
---

# ITsSbGenericNotifySink interface


## -description

Exposes methods that reports completion to and gets wait time from the Remote Desktop Connection Broker (RD Connection Broker).

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbGenericNotifySink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbGenericNotifySink</b> also has these types of members:
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
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbgenericnotifysink-getwaittimeout">GetWaitTimeout</a>
</td>
<td align="left" width="63%">
Retrieves the wait timeout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbgenericnotifysink-oncompleted">OnCompleted</a>
</td>
<td align="left" width="63%">
Reports completion to RD Connection Broker. 

</td>
</tr>
</table>