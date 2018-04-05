---
UID: NN:waasapi.IWaaSAssessor
title: IWaaSAssessor
author: windows-driver-content
description: Gets the OS update assessment by comparing the latest build from Microsoft against the build running on the current device.
old-location: base\iwaasassessor.htm
old-project: SysInfo
ms.assetid: CE5D99C9-2348-4566-AC94-DFBA5B583503
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IWaaSAssessor, IWaaSAssessor interface, IWaaSAssessor interface, described, base.iwaasassessor, waasapi/IWaaSAssessor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	waasapi.h
api_name:
-	IWaaSAssessor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IWaaSAssessor interface


## -description


Gets the OS update assessment by comparing the latest build from Microsoft against the build running on the current device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWaaSAssessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWaaSAssessor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3123362E-6A1C-49BD-BE9C-0B8506EA944B">GetOSUpdateAssessment</a>
</td>
<td align="left" width="63%">
 Gets the OS update assessment by comparing the latest release OS version from Microsoft to the OS build running on the device.

</td>
</tr>
</table> 


## -remarks



The <b>IWaaSAssessor</b> interface retrieves the <a href="https://msdn.microsoft.com/D76D0587-E31E-48D2-9DF6-33444E4CA325">OSUpdateAssessment</a>. This assessment may be cached; if there is no cached entry, the assessment will be created on demand through the WaaS Assessment Client. The client creates the assessment by contacting the WaaS Assessment Service for update information applicable to the device. The client then performs the assessment using the retrieved information. 



