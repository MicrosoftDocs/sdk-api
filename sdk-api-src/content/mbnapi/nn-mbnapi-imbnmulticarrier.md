---
UID: NN:mbnapi.IMbnMultiCarrier
title: IMbnMultiCarrier
author: windows-sdk-content
description: This interface exposes the multi-carrier functionality of a capable Mobile Broadband device.
old-location: mbn\imbnmulticarrier.htm
tech.root: mbn
ms.assetid: E40517CE-3169-4F20-A572-EDBC8FEC2862
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMbnMultiCarrier, IMbnMultiCarrier interface [Microsoft Broadband Networks], IMbnMultiCarrier interface [Microsoft Broadband Networks],described, mbn.imbnmulticarrier, mbnapi/IMbnMultiCarrier
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnMultiCarrier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnMultiCarrier interface


## -description


This interface exposes the multi-carrier functionality of a capable Mobile Broadband device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnMultiCarrier</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnMultiCarrier</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnMultiCarrier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8DA29C25-3866-4BCA-8591-F8408A1C1401">GetCurrentCellularClass</a>
</td>
<td align="left" width="63%">
Gets the current cellular classes for a multi-carrier device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91D27D4D-5838-4D6D-BECF-B336B9F3B52A">GetPreferredProviders</a>
</td>
<td align="left" width="63%">
Gets the list of subscribed providers visible in the current area for a multi-carrier device minus the current registered provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80B29D28-9940-4A96-B95A-A9640CE5E929">GetSupportedCellularClasses</a>
</td>
<td align="left" width="63%">
Gets the list of supported cellular classes for a multi-carrier device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC11D275-C6E3-48EE-B3DA-C9BC8648D49D">GetVisibleProviders</a>
</td>
<td align="left" width="63%">
Gets the list of visible providers in the current area for a multi-carrier device minus preferred and registered providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a>
</td>
<td align="left" width="63%">
Scans the network to get a list of visible providers for a multi-carrier device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a>
</td>
<td align="left" width="63%">
Updates the home provider for a multi-carrier device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c4c4bb3b-76ce-4872-8ea1-d2839cbc9b1b">MBN_CTRL_CAPS</a>
 

 

