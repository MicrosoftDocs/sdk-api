---
UID: NN:scesvc.ISceSvcAttachmentPersistInfo
title: ISceSvcAttachmentPersistInfo (scesvc.h)

description: The ISceSvcAttachmentPersistInfo interface retrieves any modified configuration or analysis information from an attachment snap-in.
old-location: security\iscesvcattachmentpersistinfo.htm
tech.root: SecMgmt
ms.assetid: 3cd4bde2-55f6-4ab1-b175-7689b0cc529b

ms.date: 12/05/2018
ms.keywords: ISceSvcAttachmentPersistInfo, ISceSvcAttachmentPersistInfo interface [Security], ISceSvcAttachmentPersistInfo interface [Security],described, _config_iscesvcattachmentpersistinfo, scesvc/ISceSvcAttachmentPersistInfo, security.iscesvcattachmentpersistinfo
ms.topic: interface
f1_keywords: 
 - "scesvc/ISceSvcAttachmentPersistInfo"
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
 - ISceSvcAttachmentPersistInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISceSvcAttachmentPersistInfo interface


## -description


The <b>ISceSvcAttachmentPersistInfo</b> interface retrieves any modified configuration or analysis information from an attachment snap-in.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISceSvcAttachmentPersistInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISceSvcAttachmentPersistInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISceSvcAttachmentPersistInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees memory allocated by the attachment snap-in extension.</p> (Inherited from <b>ISceSvcAttachmentPersistInfo</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-isdirty">IsDirty</a>
</td>
<td align="left" width="63%">
Indicates whether data stored in the attachment snap-in extension has changed since the last time the snap-in extension's data was saved.</p> (Inherited from <b>ISceSvcAttachmentPersistInfo</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-save">Save</a>
</td>
<td align="left" width="63%">
Gets the data that needs to be saved from the snap-in extension.</p> (Inherited from <b>ISceSvcAttachmentPersistInfo</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentdata">ISceSvcAttachmentData</a>
 

 

