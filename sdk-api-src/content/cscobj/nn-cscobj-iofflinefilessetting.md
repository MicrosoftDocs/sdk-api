---
UID: NN:cscobj.IOfflineFilesSetting
title: IOfflineFilesSetting (cscobj.h)
description: Represents a setting that controls the behavior the Offline Files service.
old-location: of\iofflinefilessetting.htm
tech.root: offlinefiles
ms.assetid: 6f47c67b-9438-4229-89b2-6b3f9da8fb68
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSetting, IOfflineFilesSetting interface [Offline Files], IOfflineFilesSetting interface [Offline Files],described, cscobj/IOfflineFilesSetting, of.iofflinefilessetting
ms.topic: interface
f1_keywords:
- cscobj/IOfflineFilesSetting
dev_langs:
- c++
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CscSvc.dll
- CscObj.dll
api_name:
- IOfflineFilesSetting
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSetting interface


## -description


Represents a setting that controls the behavior the Offline Files service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSetting</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesSetting</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSetting</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-deletepreference">DeletePreference</a>
</td>
<td align="left" width="63%">
Removes a preference setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves a name associated with a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getpolicy">GetPolicy</a>
</td>
<td align="left" width="63%">
Retrieves a policy associated with a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getpolicyscope">GetPolicyScope</a>
</td>
<td align="left" width="63%">
Indicates the scope of the policy associated with this setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getpreference">GetPreference</a>
</td>
<td align="left" width="63%">
Retrieves a per-machine or per-user preference associated with a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getpreferencescope">GetPreferenceScope</a>
</td>
<td align="left" width="63%">
Retrieves the scope of the preference associated with this setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getvaluetype">GetValueType</a>
</td>
<td align="left" width="63%">
Retrieves the data type of a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-setpreference">SetPreference</a>
</td>
<td align="left" width="63%">
Sets a per-computer or per-user preference associated with an Offline Files setting.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

