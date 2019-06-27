---
UID: NN:certadm.IOCSPCAConfigurationCollection
title: IOCSPCAConfigurationCollection (certadm.h)
author: windows-sdk-content
description: Represents a set of certificates for which an Online Certificate Status Protocol (OCSP) service has been configured to provide certificate status responses.
old-location: security\iocspcaconfigurationcollection.htm
tech.root: SecCrypto
ms.assetid: 4e232c34-b5ab-4269-903b-189aac5a8ddc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfigurationCollection, IOCSPCAConfigurationCollection interface [Security], IOCSPCAConfigurationCollection interface [Security],described, certadm/IOCSPCAConfigurationCollection, security.iocspcaconfigurationcollection
ms.topic: interface
f1_keywords: 
 - "certadm/IOCSPCAConfigurationCollection"
req.header: certadm.h
req.include-header: Certsrv.h
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
 - IOCSPCAConfigurationCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCSPCAConfigurationCollection interface


## -description


The <b>IOCSPCAConfigurationCollection</b> interface represents a set of certificates for which an Online Certificate Status Protocol (OCSP) service has been configured to provide certificate status responses.

Microsoft provides a default implementation of this interface in the <b>OCSPCAConfigurationCollection</b> class. A <b>OCSPCAConfigurationCollection</b> object cannot be created externally.

The default implementation of <b>IOCSPAdmin</b> creates a <b>OCSPCAConfiguration</b> object and uses its properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOCSPCAConfigurationCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IOCSPCAConfigurationCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IOCSPCAConfigurationCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-createcaconfiguration">CreateCAConfiguration</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration and adds it to the configuration set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-deletecaconfiguration">DeleteCAConfiguration</a>
</td>
<td align="left" width="63%">
Removes a named CA configuration from the configuration set.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOCSPCAConfigurationCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Gets an enumerator for the configuration set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-get_count">Count</a>


</td>
<td align="left" width="63%">
Gets the number of CA configurations  in the configuration set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-get_item">Item</a>


</td>
<td align="left" width="63%">
Gets a CA configuration identified by index  in the configuration set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-iocspcaconfigurationcollection-get_itembyname">ItemByName</a>


</td>
<td align="left" width="63%">
Gets a CA configuration identified by name in the configuration set.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

