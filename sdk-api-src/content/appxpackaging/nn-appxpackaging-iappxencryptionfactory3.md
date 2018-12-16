---
UID: NN:appxpackaging.IAppxEncryptionFactory3
title: IAppxEncryptionFactory3
author: windows-sdk-content
description: Creates objects for encrypting, decrypting, reading, and writing Windows app packages and bundles.
old-location: appxpkg\iappxencryptionfactory3.htm
tech.root: appxpkg
ms.assetid: ABF2F4BE-FC6A-4AF5-BD15-243ABFA055D9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAppxEncryptionFactory3, IAppxEncryptionFactory3 interface [App packaging and management], IAppxEncryptionFactory3 interface [App packaging and management],described, appxpackaging/IAppxEncryptionFactory3, appxpkg.iappxencryptionfactory3
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
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
 - AppxPackaging.h
api_name:
 - IAppxEncryptionFactory3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxEncryptionFactory3 interface


## -description


Creates objects for encrypting, decrypting,  reading, and writing Windows app packages and bundles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptionFactory3</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxEncryptionFactory3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptionFactory3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E12E38B-23F3-437A-B3DF-1614663CFD3F">CreateEncryptedBundleWriter</a>
</td>
<td align="left" width="63%">
Creates a write-only bundle object to which encrypted Windows app packages can be added.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9CBBAF89-DE9F-49B6-B03A-2F3B6B4CE1E4">CreateEncryptedPackageWriter</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://msdn.microsoft.com/19096DFB-A8CF-4DEF-863B-3DBB9E893A8D">IAppxEncryptedPackageWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ECF7227-08A1-4AEB-8545-420090131FB8">EncryptBundle</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app bundle from an unencrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B3FE76E-57B5-411C-BD87-B9AE3208A11D">EncryptPackage</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app package from an unencrypted one.

</td>
</tr>
</table> 

