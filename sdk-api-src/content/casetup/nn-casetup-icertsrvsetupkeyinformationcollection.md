---
UID: NN:casetup.ICertSrvSetupKeyInformationCollection
title: ICertSrvSetupKeyInformationCollection (casetup.h)

description: Defines functionality to populate and enumerate a collection of ICertSrvSetupKeyInformation objects.
old-location: security\icertsrvsetupkeyinformationcollection.htm
tech.root: SecCrypto
ms.assetid: d029dd5f-9c19-46fd-aac3-275c624a157b

ms.date: 12/05/2018
ms.keywords: ICertSrvSetupKeyInformationCollection, ICertSrvSetupKeyInformationCollection interface [Security], ICertSrvSetupKeyInformationCollection interface [Security],described, casetup/ICertSrvSetupKeyInformationCollection, security.icertsrvsetupkeyinformationcollection
ms.topic: interface
f1_keywords: 
 - "casetup/ICertSrvSetupKeyInformationCollection"
dev_langs:
 - c++
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetupKeyInformationCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertSrvSetupKeyInformationCollection interface


## -description


The <b>ICertSrvSetupKeyInformationCollection</b> interface defines functionality to populate and enumerate a collection of <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> objects. Microsoft provides an implementation of this interface in the <b>CCertSrvSetupKeyInformationCollection</b> class. You cannot create an external instance of this interface. You obtain this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getexistingcacertificates">GetExistingCACertificates</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetupKeyInformationCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICertSrvSetupKeyInformationCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertSrvSetupKeyInformationCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetupkeyinformationcollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> object to the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetupKeyInformationCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetupkeyinformationcollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetupkeyinformationcollection-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertsrvsetupkeyinformationcollection-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> object that is identified by index in the collection.

</td>
</tr>
</table> 

