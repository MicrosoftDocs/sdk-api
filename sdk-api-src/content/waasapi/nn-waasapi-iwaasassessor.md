---
UID: NN:waasapi.IWaaSAssessor
title: IWaaSAssessor (waasapi.h)
description: Gets the OS update assessment by comparing the latest build from Microsoft against the build running on the current device.
helpviewer_keywords: ["IWaaSAssessor","IWaaSAssessor interface","IWaaSAssessor interface","described","base.iwaasassessor","waasapi/IWaaSAssessor"]
old-location: base\iwaasassessor.htm
tech.root: SysInfo
ms.assetid: CE5D99C9-2348-4566-AC94-DFBA5B583503
ms.date: 12/05/2018
ms.keywords: IWaaSAssessor, IWaaSAssessor interface, IWaaSAssessor interface,described, base.iwaasassessor, waasapi/IWaaSAssessor
f1_keywords:
- waasapi/IWaaSAssessor
dev_langs:
- c++
req.header: waasapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WaaSAPI.idl
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
- waasapi.h
api_name:
- IWaaSAssessor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWaaSAssessor interface


## -description


Gets the OS update assessment by comparing the latest build from Microsoft against the build running on the current device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWaaSAssessor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWaaSAssessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWaaSAssessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment">GetOSUpdateAssessment</a>
</td>
<td align="left" width="63%">
 Gets the OS update assessment by comparing the latest release OS version from Microsoft to the OS build running on the device.

</td>
</tr>
</table> 


## -remarks



The <b>IWaaSAssessor</b> interface retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/waasapitypes/ns-waasapitypes-osupdateassessment">OSUpdateAssessment</a>. This assessment may be cached; if there is no cached entry, the assessment will be created on demand through the WaaS Assessment Client. The client creates the assessment by contacting the WaaS Assessment Service for update information applicable to the device. The client then performs the assessment using the retrieved information. 

Your code must have administrator privileges to use the <b>IWaaSAssessor</b> interface. For more details about developing applications that require administrator privileges, see [this article](/windows/win32/secauthz/developing-applications-that-require-administrator-privilege).

