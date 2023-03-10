---
UID: NF:certadm.IOCSPCAConfiguration.get_ProviderProperties
title: IOCSPCAConfiguration::get_ProviderProperties (certadm.h)
description: Gets or sets information that provides certificate status responses. (Get)
helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","ProviderProperties property","IOCSPCAConfiguration.ProviderProperties","IOCSPCAConfiguration.get_ProviderProperties","IOCSPCAConfiguration::ProviderProperties","IOCSPCAConfiguration::get_ProviderProperties","IOCSPCAConfiguration::put_ProviderProperties","ProviderProperties property [Security]","ProviderProperties property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::ProviderProperties","certadm/IOCSPCAConfiguration::get_ProviderProperties","certadm/IOCSPCAConfiguration::put_ProviderProperties","get_ProviderProperties","security.iocspcaconfiguration_providerproperties_method"]
old-location: security\iocspcaconfiguration_providerproperties_method.htm
tech.root: security
ms.assetid: 60ac0123-9696-4893-ae2a-278b4e70c098
ms.date: 3/17/2021
ms.keywords: IOCSPCAConfiguration interface [Security],ProviderProperties property, IOCSPCAConfiguration.ProviderProperties, IOCSPCAConfiguration.get_ProviderProperties, IOCSPCAConfiguration::ProviderProperties, IOCSPCAConfiguration::get_ProviderProperties, IOCSPCAConfiguration::put_ProviderProperties, ProviderProperties property [Security], ProviderProperties property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::ProviderProperties, certadm/IOCSPCAConfiguration::get_ProviderProperties, certadm/IOCSPCAConfiguration::put_ProviderProperties, get_ProviderProperties, security.iocspcaconfiguration_providerproperties_method
req.header: certadm.h
req.include-header: Certserv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPCAConfiguration::get_ProviderProperties
 - certadm/IOCSPCAConfiguration::get_ProviderProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfiguration.ProviderProperties
 - IOCSPCAConfiguration.get_ProviderProperties
 - IOCSPCAConfiguration.put_ProviderProperties
---

# IOCSPCAConfiguration::get_ProviderProperties


## -description

The <b>ProviderProperties</b> property gets or sets information that provides certificate status responses. The revocation information provider configured in the <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_providerclsid">ProviderCLSID</a> property uses <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) specified in this property to provide responses.

This property is read/write.

## -parameters

## -remarks


The <b>VARIANT</b> returned in <i>pVal</i> is a pointer to a safe array that contains the properties as name-value pairs.


This array is a two-dimensional array of elements, each of type VARIANT. The array contains one row for each named property in the collection. Each row contains two columns: the property name and the property value.


The following table lists the possible named property values and their data types for the default revocation provider:


<table>
<tr>
<th>Name</th>
<th>Data type</th>
</tr>
<tr>
<td>BaseCrl</td>
<td>REG_BINARY</td>
</tr>
<tr>
<td>BaseCrlUrls </td>
<td>REG_MULTI_SZ</td>
</tr>
<tr>
<td>CrlUrlTimeout</td>
<td>DWORD</td>
</tr>
<tr>
<td>DeltaCrl</td>
<td>REG_BINARY</td>
</tr>
<tr>
<td>DeltaCrlUrls</td>
<td>REG_MULTI_SZ</td>
</tr>
<tr>
<td>RefreshTimeOut</td>
<td>DWORD</td>
</tr>
<tr>
<td>RevocationErrorCode</td>
<td>DWORD</td>
</tr>
<tr>
<td>IssuedSerialNumbersDirectories</td>
<td>REG_MULTI_SZ</td>
</tr>
</table>

Note: IssuedSerialNumberDirectories is not supported on Windows Server 2008.


## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
