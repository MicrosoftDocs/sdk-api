---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAppxEncryptionFactory interface


## -description


Creates objects for encrypting, decrypting,  reading, and writing packages and bundles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptionFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxEncryptionFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptionFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1802E721-9320-4B05-9C38-6C3AC3FB413C">CreateEncryptedBundleReader</a>
</td>
<td align="left" width="63%">
Creates a read-only bundle object to which encrypted Windows app packages can be added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01FF3DF1-CCA8-49BF-9876-57A4DDA658D0">CreateEncryptedBundleWriter</a>
</td>
<td align="left" width="63%">
Creates a write-only bundle object to which encrypted Windows app packages can be added.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/325E4883-69D7-4E2A-A664-3CA3C5559CB3">CreateEncryptedPackageReader</a>
</td>
<td align="left" width="63%">
Creates a new instance of <a href="appxpkg.iappxencryptedpackagereader">IAppxEncryptedPackageReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01447B17-E197-4E08-B878-F5487F3E9E92">CreateEncryptedPackageWriter</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://msdn.microsoft.com/19096DFB-A8CF-4DEF-863B-3DBB9E893A8D">IAppxEncryptedPackageWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ED10EBD7-F942-4F1D-B2DC-0895022771BE">DecryptBundle</a>
</td>
<td align="left" width="63%">
Creates an unencrypted Windows app bundle from an encrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FB3BC989-F165-417A-963A-7B78B65930FA">DecryptPackage</a>
</td>
<td align="left" width="63%">
Creates an unencrypted Windows app package from an encrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F2FFBB18-4E62-4704-B252-1749058A0A5E">EncryptBundle</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app bundle from an unencrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C77A9F9-340C-4846-8EDA-26FAB7E53D60">EncryptPackage</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app package from an unencrypted one.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/E88355DA-F7BE-45C7-9DDB-EC39DB2AD280">IAppxEncryptedBundleWriter</a>



<a href="https://msdn.microsoft.com/19096DFB-A8CF-4DEF-863B-3DBB9E893A8D">IAppxEncryptedPackageWriter</a>
 

 

