---
UID: NN:gpmgmt.IGPMClientSideExtension
title: IGPMClientSideExtension
author: windows-sdk-content
description: The IGPMClientSideExtension interface supports methods that allow you to query client-side extension properties when you use the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmclientsideextension.htm
old-project: GPMC
ms.assetid: b29f4d09-60c0-4c67-b295-05c7d9a05397
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMClientSideExtension, IGPMClientSideExtension, IGPMClientSideExtension interface [GPMC], IGPMClientSideExtension interface [GPMC],described, _win32_igpmclientsideextension, gpmc.igpmclientsideextension, gpmgmt/IGPMClientSideExtension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMClientSideExtension
 - GPMClientSideExtension
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMClientSideExtension interface


## -description


The 
<b>IGPMClientSideExtension</b> interface supports methods that allow you to query client-side extension properties when you use the Group Policy Management Console (GPMC) interfaces. You can also check whether a client-side extension can be called during the processing of policy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMClientSideExtension</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMClientSideExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMClientSideExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c15ca1b0-f744-426e-a54f-402eef461227">IsComputerEnabled</a>
</td>
<td align="left" width="63%">
Checks whether a client-side extension can be called during the processing of computer policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01fba0fa-9639-4033-bbdf-704549524147">IsUserEnabled</a>
</td>
<td align="left" width="63%">
Checks whether a client-side extension can be called during the processing of user policy.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMClientSideExtension</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">DisplayName</a>


</td>
<td align="left" width="63%">
Display name of the client-side extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">ID</a>


</td>
<td align="left" width="63%">
GUID of the client-side extension.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">IGPMCSECollection</a>
 

 

