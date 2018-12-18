---
UID: NN:gpmgmt.IGPMResult
title: IGPMResult
author: windows-sdk-content
description: The IGPMResult interface contains methods to retrieve status message information while performing various types of GPO processing operations such as restore, import, copy and backup.
old-location: gpmc\igpmresult.htm
tech.root: gpmc
ms.assetid: 0228ed1a-3a8f-486a-9dd8-806ca35c649e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GPMResult, IGPMResult, IGPMResult interface [GPMC], IGPMResult interface [GPMC],described, _win32_igpmresult, gpmc.igpmresult, gpmgmt/IGPMResult
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
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMResult
 - GPMResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMResult interface


## -description


The 
<b>IGPMResult</b> interface contains methods to retrieve status message information while performing various types of GPO processing operations such as restore, import, copy and backup.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMResult</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/814c59b7-47bc-4757-997e-95ca578f544a">OverallStatus</a>
</td>
<td align="left" width="63%">
Returns the overall status of the GPMC operation.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/34b9c8da-9a5f-4415-b62e-31083578c802">Result</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Pointer to a <b>VARIANT</b> that receives the result of various types of GPO operations. This property is the location at which an <b>IDispatch</b> interface pointer can be stored.

For calls to the 
<a href="https://msdn.microsoft.com/5ba8d2f7-4989-4882-9ceb-4f77b8745442">IGPMGPO::Backup</a> method, the result is a pointer to an 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interface. For calls to 
<a href="https://msdn.microsoft.com/8e202ea1-ca5c-4757-950b-ea1802699b68">IGPMDomain::RestoreGPO</a>, 
<a href="https://msdn.microsoft.com/3b16eefb-89af-408b-a84c-c8ab958b4cc7">IGPMGPO::Import</a>, and 
<a href="https://msdn.microsoft.com/17f4c6b2-6c75-4d4c-88c5-6d9ef2cb7a07">IGPMGPO::CopyTo</a>, the result is a pointer to an 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface. For calls to the <a href="https://msdn.microsoft.com/19b3b027-59f1-4c31-896b-5b5fd23b9be4">IGPMGPO::GenerateReport</a> method, the result contains a binary string of XML or HTML.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/34b9c8da-9a5f-4415-b62e-31083578c802">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Pointer to an 
<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>
 

 

