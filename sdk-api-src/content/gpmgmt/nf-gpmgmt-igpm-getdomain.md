---
UID: NF:gpmgmt.IGPM.GetDomain
title: IGPM::GetDomain (gpmgmt.h)
description: Creates and returns a GPMDomain object that corresponds to the specified domain.
helpviewer_keywords: ["GPM object [GPMC]","GetDomain method","GetDomain","GetDomain method [GPMC]","GetDomain method [GPMC]","GPM object","GetDomain method [GPMC]","IGPM interface","IGPM interface [GPMC]","GetDomain method","IGPM.GetDomain","IGPM::GetDomain","_win32_igpm_getdomain","gpmc.igpm_getdomain","gpmgmt/IGPM::GetDomain"]
old-location: gpmc\igpm_getdomain.htm
tech.root: gpmc
ms.assetid: 32aee72f-96fa-4ebd-9ff7-643972b82cf6
ms.date: 12/05/2018
ms.keywords: GPM object [GPMC],GetDomain method, GetDomain, GetDomain method [GPMC], GetDomain method [GPMC],GPM object, GetDomain method [GPMC],IGPM interface, IGPM interface [GPMC],GetDomain method, IGPM.GetDomain, IGPM::GetDomain, _win32_igpm_getdomain, gpmc.igpm_getdomain, gpmgmt/IGPM::GetDomain
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPM::GetDomain
 - gpmgmt/IGPM::GetDomain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPM.GetDomain
 - GPM.GetDomain
---

# IGPM::GetDomain


## -description

Creates and returns a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">GPMDomain</a> object that corresponds to the specified domain.

The object allows you to do the following:
<ul>
<li>Create, query, and restore Group Policy objects (GPOs)</li>
<li>Search scope of management (SOM) objects</li>
<li>Search and retrieve Windows Management Instrumentation (WMI) filters</li>
</ul>

## -parameters

### -param bstrDomain [in]

Name of the domain specified as a string. This must be a full Domain Name System (DNS) name, such as `contoso.com`.

### -param bstrDomainController [in]

If specified, the name of the domain controller to use with the domain. The name can be a DNS name or a NetBIOS name. Otherwise, the method uses the primary domain controller (PDC). For more information, see the <i>lDCFlags</i> parameter.

<b>Scripting:  </b>This parameter must pass an empty string ("") when a domain controller is not specified.

### -param lDCFlags [in]

Flags to use to locate the domain controller for the domain. You can specify <b>GPM_USE_ANYDC</b>, <b>GPM_USE_PDC</b>, or <b>GPM_DONOTUSE_W2KDC</b>.

If this parameter is set to zero, and a <i>bstrDomainController</i> is specified, the method uses the specified <i>bstrDomainController</i>. Otherwise, the method uses the PDC.

### -param pIGPMDomain [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMDomain</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMDomain</b> object.

## -remarks

>**Important:** When calling this function, underlying LDAP traffic is encrypted using Kerberos, not SSL.

This method does not allow you to search site SOMs. Call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getsitescontainer">IGPM::GetSitesContainer</a> method to perform this type of query.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>
