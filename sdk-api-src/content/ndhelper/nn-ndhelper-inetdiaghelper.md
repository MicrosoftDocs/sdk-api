---
UID: NN:ndhelper.INetDiagHelper
title: INetDiagHelper (ndhelper.h)
description: The INetDiagHelper interface provides methods that capture and provide information associated with diagnoses and resolution of network-related issues.
helpviewer_keywords: ["INetDiagHelper","INetDiagHelper interface [NDF]","INetDiagHelper interface [NDF]","described","ndf.inetdiaghelper","ndhelper/INetDiagHelper"]
old-location: ndf\inetdiaghelper.htm
tech.root: NDF
ms.assetid: 7f1b8a5b-389b-4276-a49d-94a39be3c35c
ms.date: 12/05/2018
ms.keywords: INetDiagHelper, INetDiagHelper interface [NDF], INetDiagHelper interface [NDF],described, ndf.inetdiaghelper, ndhelper/INetDiagHelper
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetDiagHelper
 - ndhelper/INetDiagHelper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ndhelper.h
api_name:
 - INetDiagHelper
---

# INetDiagHelper interface


## -description

The <b>INetDiagHelper</b> interface provides methods that capture and provide information associated with diagnoses and resolution of network-related issues.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetDiagHelper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetDiagHelper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel">INetDiagHelper::Cancel</a>
</td>
<td align="left" width="63%">
Cancels an ongoing diagnosis or repair. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup">INetDiagHelper::Cleanup</a>
</td>
<td align="left" width="63%">
Allows NDF  to release resources. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getattributes">INetDiagHelper::GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves information from the helper class. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getcachetime">INetDiagHelper::GetCacheTime</a>
</td>
<td align="left" width="63%">
Retrieves information about the length of time results are kept in the cache. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo">INetDiagHelper::GetDiagnosticsInfo</a>
</td>
<td align="left" width="63%">
Retrieves time estimate and whether impersonation is necessary. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdownstreamhypotheses">INetDiagHelper::GetDownStreamHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information about possible causes in downstream network components. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-gethigherhypotheses">INetDiagHelper::GetHigherHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information about possible causes of high utilization in upstream network components. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getkeyattributes">INetDiagHelper::GetKeyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves information about key attributes of a helper class. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getlifetime">INetDiagHelper::GetLifeTime</a>
</td>
<td align="left" width="63%">
Retrieves information about the life time of a helper class instance. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getlowerhypotheses">INetDiagHelper::GetLowerHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information from local components about for possible causes of high utilization. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo">INetDiagHelper::GetRepairInfo</a>
</td>
<td align="left" width="63%">
Retrieves information from the helper class about resolutions or workarounds. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getupstreamhypotheses">INetDiagHelper::GetUpStreamHypotheses</a>
</td>
<td align="left" width="63%">
Retrieves information from the helper class about if it checks for high utilization. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization">INetDiagHelper::HighUtilization</a>
</td>
<td align="left" width="63%">
Allows the helper class to check for high utilization. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize">INetDiagHelper::Initialize</a>
</td>
<td align="left" width="63%">
Sends key parameters to a helper class. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth">INetDiagHelper::LowHealth</a>
</td>
<td align="left" width="63%">
Determines whether the helper class is in low health. This method is required when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair">INetDiagHelper::Repair</a>
</td>
<td align="left" width="63%">
Asks the helper class to perform the specified repair. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-setlifetime">INetDiagHelper::SetLifeTime</a>
</td>
<td align="left" width="63%">
Sets the start and end times of a problem instance. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-validate">INetDiagHelper::Validate</a>
</td>
<td align="left" width="63%">
Confirms that a previously diagnosed problem is fixed. This method is optional when building a Helper Class extension.

</td>
</tr>
</table>

