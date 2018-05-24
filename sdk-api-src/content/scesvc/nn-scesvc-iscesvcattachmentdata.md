---
UID: NN:scesvc.ISceSvcAttachmentData
title: ISceSvcAttachmentData
author: windows-driver-content
description: The ISceSvcAttachmentData interface retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins.
old-location: security\iscesvcattachmentdata.htm
old-project: SecMgmt
ms.assetid: 385acdb9-5642-47c1-b2ac-be388edaac12
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ISceSvcAttachmentData, ISceSvcAttachmentData interface [Security], ISceSvcAttachmentData interface [Security],described, _config_iscesvcattachmentdata, scesvc/ISceSvcAttachmentData, security.iscesvcattachmentdata
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
-	ISceSvcAttachmentData
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISceSvcAttachmentData interface


## -description


The <b>ISceSvcAttachmentData</b> interface retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISceSvcAttachmentData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISceSvcAttachmentData</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e50f5acf-06ef-49bb-bcf1-1fadeb4b808a">CloseHandle</a>
</td>
<td align="left" width="63%">
Closes the handle to the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3645547e-5d6e-42df-802b-cf8b1a4c1e11">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees a data buffer allocated by the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
</td>
<td align="left" width="63%">
Retrieves data from the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a connection to the Security Configuration snap-in.</p> (Inherited from <b>IsceSvcAttachmentData</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3cd4bde2-55f6-4ab1-b175-7689b0cc529b">ISceSvcAttachmentPersistInfo</a>
 

 

