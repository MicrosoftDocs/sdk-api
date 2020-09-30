---
UID: NN:storageprovider.IStorageProviderPropertyHandler
title: IStorageProviderPropertyHandler (storageprovider.h)
description: Provides a collection of properties associated with a file or folder.
helpviewer_keywords: ["IStorageProviderPropertyHandler","IStorageProviderPropertyHandler interface [Windows Shell]","IStorageProviderPropertyHandler interface [Windows Shell]","described","shell.istorageproviderpropertyhandler","storageprovider/IStorageProviderPropertyHandler"]
old-location: shell\istorageproviderpropertyhandler.htm
tech.root: shell
ms.assetid: 8CB56726-DABA-44A4-ADAE-DAD8ECB047E6
ms.date: 12/05/2018
ms.keywords: IStorageProviderPropertyHandler, IStorageProviderPropertyHandler interface [Windows Shell], IStorageProviderPropertyHandler interface [Windows Shell],described, shell.istorageproviderpropertyhandler, storageprovider/IStorageProviderPropertyHandler
req.header: storageprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorageProviderPropertyHandler
 - storageprovider/IStorageProviderPropertyHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - storageprovider.h
api_name:
 - IStorageProviderPropertyHandler
---

# IStorageProviderPropertyHandler interface


## -description

Provides a collection of properties associated with a file or folder.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStorageProviderPropertyHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStorageProviderPropertyHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStorageProviderPropertyHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/storageprovider/nf-storageprovider-istorageproviderpropertyhandler-retrieveproperties">RetrieveProperties</a>
</td>
<td align="left" width="63%">
Gets the properties managed by the sync engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/shell/istorageproviderpropertyhandler-saveproperties">SaveProperties</a>
</td>
<td align="left" width="63%">
Saves properties associated with a file or folder.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Caution</b>  <p class="note">You should only implement this interface if you have a specific need to do so.  

</div>
<div> </div>
This interface can be implemented by a cloud storage provider sync engine to share properties about a file or file folder. An instance of <b>IStorageProviderPropertyHandler</b> exists for the lifetime of a storage file created under a sync root. Use <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler">IStorageProviderHandler</a> to retrieve the set of properties associated with an individual file or folder.

This interface is responsible for keeping track of the following properties:

<ul>
<li>StorageProviderFileIdentifier</li>
<li>StorageProviderFileRemoteUri</li>
<li>StorageProviderFileChecksum</li>
<li>StorageProviderFileVersionWaterline</li>
</ul>