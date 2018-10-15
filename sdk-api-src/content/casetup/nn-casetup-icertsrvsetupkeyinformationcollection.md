---
UID: NN:casetup.ICertSrvSetupKeyInformationCollection
title: ICertSrvSetupKeyInformationCollection
author: windows-sdk-content
description: Defines functionality to populate and enumerate a collection of ICertSrvSetupKeyInformation objects.
old-location: security\icertsrvsetupkeyinformationcollection.htm
tech.root: seccrypto
ms.assetid: d029dd5f-9c19-46fd-aac3-275c624a157b
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ICertSrvSetupKeyInformationCollection, ICertSrvSetupKeyInformationCollection interface [Security], ICertSrvSetupKeyInformationCollection interface [Security],described, casetup/ICertSrvSetupKeyInformationCollection, security.icertsrvsetupkeyinformationcollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetupKeyInformationCollection interface


## -description


The <b>ICertSrvSetupKeyInformationCollection</b> interface defines functionality to populate and enumerate a collection of <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> objects. Microsoft provides an implementation of this interface in the <b>CCertSrvSetupKeyInformationCollection</b> class. You cannot create an external instance of this interface. You obtain this interface by calling the <a href="https://msdn.microsoft.com/fd8c7bac-b6db-41f2-a648-e01ebd09c41c">GetExistingCACertificates</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetupKeyInformationCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICertSrvSetupKeyInformationCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8f342787-13f7-4bca-8320-61bb5112ee34">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> object to the collection.

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

<a href="https://msdn.microsoft.com/80a34341-176d-4040-bc60-79ce81b917b2">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/58412a07-7e97-4379-b052-fb7458400be9">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2ae3d695-4dfe-4c72-8e66-64dce88c2bb2">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> object that is identified by index in the collection.

</td>
</tr>
</table> 

