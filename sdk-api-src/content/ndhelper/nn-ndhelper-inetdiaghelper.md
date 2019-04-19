---
UID: NN:ndhelper.INetDiagHelper
title: INetDiagHelper (ndhelper.h)
author: windows-sdk-content
description: The INetDiagHelper interface provides methods that capture and provide information associated with diagnoses and resolution of network-related issues.
old-location: ndf\inetdiaghelper.htm
tech.root: NDF
ms.assetid: 7f1b8a5b-389b-4276-a49d-94a39be3c35c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetDiagHelper, INetDiagHelper interface [NDF], INetDiagHelper interface [NDF],described, ndf.inetdiaghelper, ndhelper/INetDiagHelper
ms.topic: interface
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ndhelper.h
api_name:
 - INetDiagHelper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetDiagHelper interface


## -description


The <b>INetDiagHelper</b> interface provides methods that capture and provide information associated with diagnoses and resolution of network-related issues.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetDiagHelper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetDiagHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetDiagHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0df79e75-f3a6-43fd-82a3-2798ac1d99cd">INetDiagHelper::Cancel</a>
</td>
<td align="left" width="63%">
Cancels an ongoing diagnosis or repair. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d50d3415-8fa7-404c-8030-8ea7a59820e4">INetDiagHelper::Cleanup</a>
</td>
<td align="left" width="63%">
Allows NDF  to release resources. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f1f371a-853f-4022-808b-eea01aee4a52">INetDiagHelper::GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves information from the helper class. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0298bf84-374e-438f-8141-3298e1004c1b">INetDiagHelper::GetCacheTime</a>
</td>
<td align="left" width="63%">
Retrieves information about the length of time results are kept in the cache. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc162b1b-a22e-4ee3-96a6-c2eecc13e479">INetDiagHelper::GetDiagnosticsInfo</a>
</td>
<td align="left" width="63%">
Retrieves time estimate and whether impersonation is necessary. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac26fbb5-d30f-4b1f-b432-043a07bfa853">INetDiagHelper::GetDownStreamHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information about possible causes in downstream network components. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/608b1752-4bf9-4a7d-bc20-82d89b33b306">INetDiagHelper::GetHigherHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information about possible causes of high utilization in upstream network components. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9501450-a883-4941-a03f-ab735acca82f">INetDiagHelper::GetKeyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves information about key attributes of a helper class. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0710b8d3-04d6-434f-9b0a-22049bf00ba0">INetDiagHelper::GetLifeTime</a>
</td>
<td align="left" width="63%">
Retrieves information about the life time of a helper class instance. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d17f5241-6efb-45a7-b355-8343e48b3261">INetDiagHelper::GetLowerHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information from local components about for possible causes of high utilization. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a14b1f61-1ac7-4ee7-ad82-e0821f43a17d">INetDiagHelper::GetRepairInfo</a>
</td>
<td align="left" width="63%">
Retrieves information from the helper class about resolutions or workarounds. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e683a2eb-8dec-47e2-ae3d-6c12a9b2773d">INetDiagHelper::GetUpStreamHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information from the helper class about if it checks for high utilization. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a555683-f7fd-43a4-808a-60579723293c">INetDiagHelper::HighUtilization</a>
</td>
<td align="left" width="63%">
Allows the helper class to check for high utilization. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32003720-ca59-4203-a78c-9e40c626c9f8">INetDiagHelper::Initialize</a>
</td>
<td align="left" width="63%">
Sends key parameters to a helper class. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/623de90f-c2dc-4879-9baf-4051d2d3691c">INetDiagHelper::LowHealth</a>
</td>
<td align="left" width="63%">
Determines whether the helper class is in low health. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1892cbc8-01fd-4536-b29e-de733b0f6732">INetDiagHelper::Repair</a>
</td>
<td align="left" width="63%">
Asks the helper class to perform the specified repair. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a211c885-364f-4ba5-a4c9-88a87b30cdc7">INetDiagHelper::SetLifeTime</a>
</td>
<td align="left" width="63%">
Sets the start and end times of a problem instance. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2faab163-5684-4b10-b62d-7e22d5b789a8">INetDiagHelper::Validate</a>
</td>
<td align="left" width="63%">
Confirms that a previously diagnosed problem is fixed. This method is optional when building a Helper Class extension.

</td>
</tr>
</table> 

