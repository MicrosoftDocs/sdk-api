---
UID: NN:gpmgmt.IGPMSOM
title: IGPMSOM (gpmgmt.h)
author: windows-sdk-content
description: The IGPMSOM interface contains methods that allow you to create and retrieve GPO links for a scope of management (SOM), and to set and retrieve security attributes and various properties for a SOM. A SOM can be a site, domain or OU.
old-location: gpmc\igpmsom.htm
tech.root: gpmc
ms.assetid: e3252dba-403d-486d-b666-9bb04ec0aa90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMSOM, IGPMSOM, IGPMSOM interface [GPMC], IGPMSOM interface [GPMC],described, _win32_igpmsom, gpmc.igpmsom, gpmgmt/IGPMSOM
ms.topic: interface
f1_keywords: 
 - "gpmgmt/IGPMSOM"
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
 - IGPMSOM
 - GPMSOM
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMSOM interface


## -description


The 
<b>IGPMSOM</b> interface contains methods that allow you to create and retrieve GPO links for a scope of management (SOM), and to set and retrieve security attributes and various properties for a SOM. A SOM can be a site, domain or OU.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSOM</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMSOM</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMSOM</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsom-creategpolink">CreateGPOLink</a>
</td>
<td align="left" width="63%">
Links a GPO to the specified position and sets various link-specific properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsom-getgpolinks">GetGPOLinks</a>
</td>
<td align="left" width="63%">
Returns a collection of GPO links for the SOM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsom-getinheritedgpolinks">GetInheritedGPOLinks</a>
</td>
<td align="left" width="63%">
Returns a collection of GPO links that are applied to the SOM, including links inherited from parent containers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsom-getsecurityinfo">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Returns a collection of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">GPMPermission</a> objects for the SOM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsom-setsecurityinfo">SetSecurityInfo</a>
</td>
<td align="left" width="63%">
Sets the list of permissions for the SOM.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSOM</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmsom-property-methods">GPOInheritanceBlocked</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Value that specifies whether GPO inheritance is blocked for the SOM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmsom-property-methods">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the SOM.

If IGPMSOM points to an OU, as in "Ou=testou,dc=example,dc=Microsoft,dc=com", this property is the last part of the name, that is, testou. If IGPMSOM points to a domain, as in "dc=example,dc=Microsoft,dc=com", this property is "example.microsoft.com". If it points to a site, this property is the website name; for example, "Default-first-site-name".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmsom-property-methods">Path</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Distinguished name of the SOM; for example, "ou=MyOU,dc=coname,dc=com".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmsom-property-methods">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Type of the SOM. The following types are defined:

<ul>
<li><b>somSite</b></li>
<li><b>somDomain</b></li>
<li><b>somOU</b></li>
</ul>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>
 

 

