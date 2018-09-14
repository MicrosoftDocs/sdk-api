---
UID: NF:certadm.IOCSPCAConfiguration.put_ProviderProperties
title: IOCSPCAConfiguration::put_ProviderProperties
author: windows-sdk-content
description: Gets or sets information that provides certificate status responses.
old-location: security\iocspcaconfiguration_providerproperties_method.htm
tech.root: seccrypto
ms.assetid: 60ac0123-9696-4893-ae2a-278b4e70c098
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IOCSPCAConfiguration interface [Security],ProviderProperties property, IOCSPCAConfiguration.ProviderProperties, IOCSPCAConfiguration.put_ProviderProperties, IOCSPCAConfiguration::ProviderProperties, IOCSPCAConfiguration::get_ProviderProperties, IOCSPCAConfiguration::put_ProviderProperties, ProviderProperties property [Security], ProviderProperties property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::ProviderProperties, certadm/IOCSPCAConfiguration::get_ProviderProperties, certadm/IOCSPCAConfiguration::put_ProviderProperties, put_ProviderProperties, security.iocspcaconfiguration_providerproperties_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPCAConfiguration::put_ProviderProperties


## -description


The <b>ProviderProperties</b> property gets or sets information that provides certificate status responses. The revocation information provider configured in the <a href="https://msdn.microsoft.com/en-us/library/Aa386369(v=VS.85).aspx">ProviderCLSID</a> property uses <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation lists</a> (CRLs) specified in this property to provide responses.

This property is read/write.


## -parameters


## -remarks



The <b>VARIANT</b> returned in <i>pVal</i> is an <a href="https://msdn.microsoft.com/en-us/library/Aa386394(v=VS.85).aspx">IOCSPPropertyCollection</a> interface.

To work with revocation-information provider properties:

<ol>
<li>Create an <a href="https://msdn.microsoft.com/en-us/library/Aa386394(v=VS.85).aspx">IOCSPPropertyCollection</a> object.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Aa386413(v=VS.85).aspx">InitializeFromProperties</a> and pass in the <b>VARIANT</b>, <i>pVal</i>, returned by the <b>ProviderProperties</b> property.</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/Bb394801(v=VS.85).aspx">Methods</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb394806(v=VS.85).aspx">Properties</a> of the <a href="https://msdn.microsoft.com/en-us/library/Aa386394(v=VS.85).aspx">IOCSPPropertyCollection</a> interface.</li>
</ol>
The following table lists the possible <a href="https://msdn.microsoft.com/en-us/library/Aa386391(v=VS.85).aspx">IOCSPProperty</a> <a href="https://msdn.microsoft.com/en-us/library/Aa386543(v=VS.85).aspx">Name</a> values and their data types for the default revocation-information provider.

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




<a href="https://msdn.microsoft.com/en-us/library/Aa386328(v=VS.85).aspx">IOCSPCAConfiguration</a>
 

 

