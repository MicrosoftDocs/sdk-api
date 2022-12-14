---
UID: NF:certadm.IOCSPCAConfiguration.put_ProviderProperties
title: IOCSPCAConfiguration::put_ProviderProperties (certadm.h)
description: Gets or sets information that provides certificate status responses. (Put)
helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","ProviderProperties property","IOCSPCAConfiguration.ProviderProperties","IOCSPCAConfiguration.put_ProviderProperties","IOCSPCAConfiguration::ProviderProperties","IOCSPCAConfiguration::get_ProviderProperties","IOCSPCAConfiguration::put_ProviderProperties","ProviderProperties property [Security]","ProviderProperties property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::ProviderProperties","certadm/IOCSPCAConfiguration::get_ProviderProperties","certadm/IOCSPCAConfiguration::put_ProviderProperties","put_ProviderProperties","security.iocspcaconfiguration_providerproperties_method"]
old-location: security\iocspcaconfiguration_providerproperties_method.htm
tech.root: security
ms.assetid: 60ac0123-9696-4893-ae2a-278b4e70c098
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],ProviderProperties property, IOCSPCAConfiguration.ProviderProperties, IOCSPCAConfiguration.put_ProviderProperties, IOCSPCAConfiguration::ProviderProperties, IOCSPCAConfiguration::get_ProviderProperties, IOCSPCAConfiguration::put_ProviderProperties, ProviderProperties property [Security], ProviderProperties property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::ProviderProperties, certadm/IOCSPCAConfiguration::get_ProviderProperties, certadm/IOCSPCAConfiguration::put_ProviderProperties, put_ProviderProperties, security.iocspcaconfiguration_providerproperties_method
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
 - IOCSPCAConfiguration::put_ProviderProperties
 - certadm/IOCSPCAConfiguration::put_ProviderProperties
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

# IOCSPCAConfiguration::put_ProviderProperties


## -description

The <b>ProviderProperties</b> property gets or sets information that provides certificate status responses. The revocation information provider configured in the <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_providerclsid">ProviderCLSID</a> property uses <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) specified in this property to provide responses.

This property is read/write.

## -parameters

## -remarks

The <b>VARIANT</b> returned in <i>pVal</i> is an <a href="/windows/desktop/api/certadm/nn-certadm-iocsppropertycollection">IOCSPPropertyCollection</a> interface.

To work with revocation-information provider properties:

<ol>
<li>Create an <a href="/windows/desktop/api/certadm/nn-certadm-iocsppropertycollection">IOCSPPropertyCollection</a> object.</li>
<li>Call <a href="/windows/desktop/api/certadm/nf-certadm-iocsppropertycollection-initializefromproperties">InitializeFromProperties</a> and pass in the <b>VARIANT</b>, <i>pVal</i>, returned by the <b>ProviderProperties</b> property.</li>
<li>Use the <a href="/windows/desktop/SecCrypto/methods-of-iocsppropertycollection">Methods</a> and <a href="/windows/desktop/SecCrypto/properties-of-iocsppropertycollection">Properties</a> of the <a href="/windows/desktop/api/certadm/nn-certadm-iocsppropertycollection">IOCSPPropertyCollection</a> interface.</li>
</ol>
The following table lists the possible <a href="/windows/desktop/api/certadm/nn-certadm-iocspproperty">IOCSPProperty</a> <a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_name">Name</a> values and their data types for the default revocation-information provider.

<table>
<tr>
<th>Name</th>
<th>Data type</th>
</tr>
<tr>
<td>BaseCrl</td>
<td>Depends on BaseCrlUrl</td>
</tr>
<tr>
<td>BaseCrlUrl </td>
<td>REG_MULTI_SZ</td>
</tr>
<tr>
<td>CrlUrlTimeout</td>
<td>DWORD</td>
</tr>
<tr>
<td>DeltaCrl</td>
<td>Depends on BaseCrlUrl or DeltaCrlUrl</td>
</tr>
<tr>
<td>DeltaCrlUrl</td>
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
</table>

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
