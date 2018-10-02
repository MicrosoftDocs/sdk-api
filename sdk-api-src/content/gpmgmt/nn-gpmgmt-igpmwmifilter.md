---
UID: NN:gpmgmt.IGPMWMIFilter
title: IGPMWMIFilter
author: windows-sdk-content
description: The IGPMWMIFilter interface contains methods that allow you to set and retrieve security attributes and various properties for a WMI filter. WMI filter queries are specified using WMI Query Language (WQL).
old-location: gpmc\igpmwmifilter.htm
tech.root: GPMC
ms.assetid: 801428f1-9ce5-4348-acab-23cc9ea8cac3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMWMIFilter, IGPMWMIFilter, IGPMWMIFilter interface [GPMC], IGPMWMIFilter interface [GPMC],described, _win32_igpmwmifilter, gpmc.igpmwmifilter, gpmgmt/IGPMWMIFilter
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
 - IGPMWMIFilter
 - GPMWMIFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMWMIFilter interface


## -description


The 
<b>IGPMWMIFilter</b> interface contains methods that allow you to set and retrieve security attributes and various properties for a WMI filter. WMI filter queries are specified using WMI Query Language (WQL).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMWMIFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMWMIFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMWMIFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea20dc00-fb6d-44dc-81ad-e9aa2040f3ed">GetQueryList</a>
</td>
<td align="left" width="63%">
Returns the query list stored in the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c576c842-53ce-40af-8dba-4f15e25cf493">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Returns the list of permissions for the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e03af7ce-dec8-4390-9880-6f5ff050ca0c">SetSecurityInfo</a>
</td>
<td align="left" width="63%">
Sets the list of permissions for the WMI filter.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMWMIFilter</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/237f235f-f6b1-41b5-95cf-73f512484a68">Description</a>


</td>
<td align="left" width="63%">
Description of the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/237f235f-f6b1-41b5-95cf-73f512484a68">Name</a>


</td>
<td align="left" width="63%">
Name of the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/237f235f-f6b1-41b5-95cf-73f512484a68">Path</a>


</td>
<td align="left" width="63%">
WMI path to the instance of the WMI filter; for example, MSFT_SomFilter.ID="{&lt;Guid&gt;}",Domain="&lt;Domain DNS Name&gt;".

</td>
</tr>
</table> 


## -remarks



For information about importing, exporting, and copying WMI filters, see the 
<a href="https://msdn.microsoft.com/7e874e9a-7417-4b3f-95c5-398fe92bfdf8">IWbemClassObject::GetObjectText</a> and 
<a href="https://msdn.microsoft.com/7f3cc061-839e-49c2-a225-452719f155a9">IMofCompiler::CompileBuffer</a> methods in the WMI SDK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">IGPMWMIFilterCollection</a>
 

 

