---
UID: NN:appxpackaging.IAppxEncryptedPackageWriter
title: IAppxEncryptedPackageWriter (appxpackaging.h)
author: windows-sdk-content
description: Provides a write-only object model for encrypted app packages.
old-location: appxpkg\iappxencryptedpackagewriter.htm
tech.root: appxpkg
ms.assetid: 19096DFB-A8CF-4DEF-863B-3DBB9E893A8D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxEncryptedPackageWriter, IAppxEncryptedPackageWriter interface [App packaging and management], IAppxEncryptedPackageWriter interface [App packaging and management],described, appxpackaging/IAppxEncryptedPackageWriter, appxpkg.iappxencryptedpackagewriter
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxEncryptedPackageWriter"
dev_langs:
 - c++
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
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
 - IAppxEncryptedPackageWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxEncryptedPackageWriter interface


## -description


Provides a write-only object model for encrypted app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptedPackageWriter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxEncryptedPackageWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptedPackageWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptedpackagewriter-addpayloadfileencrypted">AddPayloadFileEncrypted</a>
</td>
<td align="left" width="63%">
Adds a new encrypted payload file to the appx package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptedpackagewriter-close">Close</a>
</td>
<td align="left" width="63%">
Closes and finalizes the written package stream.

</td>
</tr>
</table> 

