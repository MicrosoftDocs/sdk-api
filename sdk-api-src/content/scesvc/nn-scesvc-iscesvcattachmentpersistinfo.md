---
UID: NN:scesvc.ISceSvcAttachmentPersistInfo
title: ISceSvcAttachmentPersistInfo
author: windows-driver-content
description: The ISceSvcAttachmentPersistInfo interface retrieves any modified configuration or analysis information from an attachment snap-in.
old-location: security\iscesvcattachmentpersistinfo.htm
old-project: SecMgmt
ms.assetid: 3cd4bde2-55f6-4ab1-b175-7689b0cc529b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ISceSvcAttachmentPersistInfo, ISceSvcAttachmentPersistInfo interface [Security], ISceSvcAttachmentPersistInfo interface [Security], described, _config_iscesvcattachmentpersistinfo, scesvc/ISceSvcAttachmentPersistInfo, security.iscesvcattachmentpersistinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: SCESVC_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsecedit.dll
api_name:
-	ISceSvcAttachmentPersistInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISceSvcAttachmentPersistInfo interface


## -description


The <b>ISceSvcAttachmentPersistInfo</b> interface retrieves any modified configuration or analysis information from an attachment snap-in.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISceSvcAttachmentPersistInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISceSvcAttachmentPersistInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b41f01a4-dc38-4954-a3c5-19fa72910d6f">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees memory allocated by the attachment snap-in extension.</p> (Inherited from <b>ISceSvcAttachmentPersistInfo</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b430e598-e16c-47fc-8f19-fbcfc6b71337">IsDirty</a>
</td>
<td align="left" width="63%">
Indicates whether data stored in the attachment snap-in extension has changed since the last time the snap-in extension's data was saved.</p> (Inherited from <b>ISceSvcAttachmentPersistInfo</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
Gets the data that needs to be saved from the snap-in extension.</p> (Inherited from <b>ISceSvcAttachmentPersistInfo</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/385acdb9-5642-47c1-b2ac-be388edaac12">ISceSvcAttachmentData</a>
 

 

