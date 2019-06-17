---
UID: NN:syncregistration.ISyncRegistrationChange
title: ISyncRegistrationChange (syncregistration.h)
author: windows-sdk-content
description: Represents a change to the registration of a synchronization provider or a synchronization provider configuration UI. The changes are reported as registration events.
old-location: winsync\isyncregistrationchange.htm
tech.root: winsync
ms.assetid: 45376bd2-1f5f-4f4c-9c4c-f5add9438d5c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncRegistrationChange, ISyncRegistrationChange interface [Windows Sync], ISyncRegistrationChange interface [Windows Sync],described, syncregistration/ISyncRegistrationChange, winsync.isyncregistrationchange
ms.topic: interface
f1_keywords: ["syncregistration/ISyncRegistrationChange"]
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncRegistrationChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncRegistrationChange interface


## -description


Represents a change to the registration of a synchronization provider or a synchronization provider configuration UI. The changes are reported as registration events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncRegistrationChange</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncRegistrationChange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncRegistrationChange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncregistrationchange-getevent">GetEvent</a>
</td>
<td align="left" width="63%">
Gets the next pending registration event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncregistrationchange-getinstanceid">GetInstanceId</a>
</td>
<td align="left" width="63%">
Gets the instance ID of the synchronization provider or synchronization provider configuration UI associated with the event.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
 

 

