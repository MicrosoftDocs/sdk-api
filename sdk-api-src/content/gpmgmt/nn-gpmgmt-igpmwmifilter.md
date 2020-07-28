---
UID: NN:gpmgmt.IGPMWMIFilter
title: IGPMWMIFilter (gpmgmt.h)
description: The IGPMWMIFilter interface contains methods that allow you to set and retrieve security attributes and various properties for a WMI filter. WMI filter queries are specified using WMI Query Language (WQL).
helpviewer_keywords: ["GPMWMIFilter","IGPMWMIFilter","IGPMWMIFilter interface [GPMC]","IGPMWMIFilter interface [GPMC]","described","_win32_igpmwmifilter","gpmc.igpmwmifilter","gpmgmt/IGPMWMIFilter"]
old-location: gpmc\igpmwmifilter.htm
tech.root: gpmc
ms.assetid: 801428f1-9ce5-4348-acab-23cc9ea8cac3
ms.date: 12/05/2018
ms.keywords: GPMWMIFilter, IGPMWMIFilter, IGPMWMIFilter interface [GPMC], IGPMWMIFilter interface [GPMC],described, _win32_igpmwmifilter, gpmc.igpmwmifilter, gpmgmt/IGPMWMIFilter
f1_keywords:
- gpmgmt/IGPMWMIFilter
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMWMIFilter interface


## -description


The 
<b>IGPMWMIFilter</b> interface contains methods that allow you to set and retrieve security attributes and various properties for a WMI filter. WMI filter queries are specified using WMI Query Language (WQL).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMWMIFilter</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMWMIFilter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmwmifilter-getquerylist">GetQueryList</a>
</td>
<td align="left" width="63%">
Returns the query list stored in the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmwmifilter-getsecurityinfo">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Returns the list of permissions for the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmwmifilter-setsecurityinfo">SetSecurityInfo</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmwmifilter-property-methods">Description</a>


</td>
<td align="left" width="63%">
Description of the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmwmifilter-property-methods">Name</a>


</td>
<td align="left" width="63%">
Name of the WMI filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmwmifilter-property-methods">Path</a>


</td>
<td align="left" width="63%">
WMI path to the instance of the WMI filter; for example, MSFT_SomFilter.ID="{&lt;Guid&gt;}",Domain="&lt;Domain DNS Name&gt;".

</td>
</tr>
</table> 


## -remarks



For information about importing, exporting, and copying WMI filters, see the 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext">IWbemClassObject::GetObjectText</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-imofcompiler-compilebuffer">IMofCompiler::CompileBuffer</a> methods in the WMI SDK.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>
 

 

