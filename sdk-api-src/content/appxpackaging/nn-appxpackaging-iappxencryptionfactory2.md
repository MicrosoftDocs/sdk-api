---
UID: NN:appxpackaging.IAppxEncryptionFactory2
title: IAppxEncryptionFactory2
author: windows-sdk-content
description: Creates objects for encrypting, decrypting, reading, and writing Windows app packages and bundles.
old-location: appxpkg\iappxencryptionfactory2.htm
tech.root: appxpkg
ms.assetid: CEA749C5-1DD0-4207-83BA-905B8838A923
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAppxEncryptionFactory2, IAppxEncryptionFactory2 interface [App packaging and management], IAppxEncryptionFactory2 interface [App packaging and management],described, appxpackaging/IAppxEncryptionFactory2, appxpkg.iappxencryptionfactory2
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxEncryptionFactory2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxEncryptionFactory2 interface


## -description


Creates objects for encrypting, decrypting,  reading, and writing Windows app packages and bundles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptionFactory2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxEncryptionFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptionFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70C3B332-7FB5-49CD-B0E2-43FD44AFF813">CreateEncryptedPackageWriter</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://msdn.microsoft.com/19096DFB-A8CF-4DEF-863B-3DBB9E893A8D">IAppxEncryptedPackageWriter</a>.

</td>
</tr>
</table> 

