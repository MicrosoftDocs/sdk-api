---
UID: NN:storageprovider.IStorageProviderHandler
title: IStorageProviderHandler (storageprovider.h)
author: windows-sdk-content
description: Retrieves the IStorageProviderPropertyHandler associated with a specific file or folder.
old-location: shell\istorageproviderhandler.htm
tech.root: shell
ms.assetid: 96DEA181-8506-4FCC-85E0-A2EF79BA6C6D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStorageProviderHandler, IStorageProviderHandler interface [Windows Shell], IStorageProviderHandler interface [Windows Shell],described, shell.istorageproviderhandler, storageprovider/IStorageProviderHandler
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - storageprovider.h
api_name:
 - IStorageProviderHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorageProviderHandler interface


## -description


Retrieves the <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> associated with a specific file or folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStorageProviderHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStorageProviderHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStorageProviderHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EBC5567-E64E-47FC-A5A9-C482714401D8">GetPropertyHandlerFromFileId</a>
</td>
<td align="left" width="63%">
Gets an instance of <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> associated with the provided file identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E02B43AC-73A8-4FD0-BC54-47922CA5EEDB">GetPropertyHandlerFromPath</a>
</td>
<td align="left" width="63%">
Gets an instance of <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> associated with the provided path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C02A9690-1E98-4960-B5E7-E75BDAAF9A62">GetPropertyHandlerFromUri</a>
</td>
<td align="left" width="63%">
Gets an instance of <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> associated with the provided URI.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Caution</b>  <p class="note">You should only implement this interface if you have a specific need to do so.  

</div>
<div> </div>


