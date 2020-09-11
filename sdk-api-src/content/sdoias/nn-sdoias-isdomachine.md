---
UID: NN:sdoias.ISdoMachine
title: ISdoMachine (sdoias.h)
description: Use the ISdoMachine interface to attach to an SDO computer, obtain information about the SDO computer, and obtain interfaces to other SDO objects.
helpviewer_keywords: ["ISdoMachine","ISdoMachine interface [Network Policy Server]","ISdoMachine interface [Network Policy Server]","described","_sdo_isdomachine","nps.SDO_isdomachine","sdo.isdomachine","sdoias/ISdoMachine"]
old-location: nps\SDO_isdomachine.htm
tech.root: Nps
ms.assetid: 11372116-56eb-4d8e-8f28-4402835ee903
ms.date: 12/05/2018
ms.keywords: ISdoMachine, ISdoMachine interface [Network Policy Server], ISdoMachine interface [Network Policy Server],described, _sdo_isdomachine, nps.SDO_isdomachine, sdo.isdomachine, sdoias/ISdoMachine
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdoMachine
 - sdoias/ISdoMachine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoMachine
---

# ISdoMachine interface


## -description

Use the 
<b>ISdoMachine</b> interface to attach to an SDO computer, obtain information about the SDO computer, and obtain interfaces to other SDO objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdoMachine</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISdoMachine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISdoMachine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">Attach</a>
</td>
<td align="left" width="63%">
Attaches to a computer in order to administer services on it through SDO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer">GetAttachedComputer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the currently attached computer, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getdictionarysdo">GetDictionarySDO</a>
</td>
<td align="left" width="63%">
Retrieves an interface for an attribute-dictionary SDO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getdomaintype">GetDomainType</a>
</td>
<td align="left" width="63%">
Retrieves the type of domain, if any, in which the SDO computer resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getostype">GetOSType</a>
</td>
<td align="left" width="63%">
Retrieves the type of operating system running on the SDO computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">GetServiceSDO</a>
</td>
<td align="left" width="63%">
Retrieves an interface for the NPS or for the RAS service SDO.

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo">GetUserSDO</a>
</td>
<td align="left" width="63%">
Retrieves an interface for a user SDO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-isdirectoryavailable">IsDirectoryAvailable</a>
</td>
<td align="left" width="63%">
Tests whether an Active Directory service is available on the SDO computer.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-server-data-objects-interfaces">Server Data Objects Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-server-data-objects-reference">Server Data Objects Reference</a>

