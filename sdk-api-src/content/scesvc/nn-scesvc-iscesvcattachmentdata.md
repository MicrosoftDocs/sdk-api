---
UID: NN:scesvc.ISceSvcAttachmentData
title: ISceSvcAttachmentData (scesvc.h)
description: The ISceSvcAttachmentData interface retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins.
helpviewer_keywords: ["ISceSvcAttachmentData","ISceSvcAttachmentData interface [Security]","ISceSvcAttachmentData interface [Security]","described","_config_iscesvcattachmentdata","scesvc/ISceSvcAttachmentData","security.iscesvcattachmentdata"]
old-location: security\iscesvcattachmentdata.htm
tech.root: security
ms.assetid: 385acdb9-5642-47c1-b2ac-be388edaac12
ms.date: 12/05/2018
ms.keywords: ISceSvcAttachmentData, ISceSvcAttachmentData interface [Security], ISceSvcAttachmentData interface [Security],described, _config_iscesvcattachmentdata, scesvc/ISceSvcAttachmentData, security.iscesvcattachmentdata
f1_keywords:
- scesvc/ISceSvcAttachmentData
dev_langs:
- c++
req.header: scesvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Wsecedit.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsecedit.dll
api_name:
- ISceSvcAttachmentData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISceSvcAttachmentData interface


## -description


The <b>ISceSvcAttachmentData</b> interface retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISceSvcAttachmentData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISceSvcAttachmentData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISceSvcAttachmentData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-closehandle">CloseHandle</a>
</td>
<td align="left" width="63%">
Closes the handle to the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees a data buffer allocated by the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-getdata">GetData</a>
</td>
<td align="left" width="63%">
Retrieves data from the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a connection to the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentpersistinfo">ISceSvcAttachmentPersistInfo</a>
 

 

