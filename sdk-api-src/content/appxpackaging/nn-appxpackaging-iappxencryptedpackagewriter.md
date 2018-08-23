---
UID: NN:appxpackaging.IAppxEncryptedPackageWriter
title: IAppxEncryptedPackageWriter
author: windows-sdk-content
description: Provides a write-only object model for encrypted app packages.
old-location: appxpkg\iappxencryptedpackagewriter.htm
old-project: appxpkg
ms.assetid: 19096DFB-A8CF-4DEF-863B-3DBB9E893A8D
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: IAppxEncryptedPackageWriter, IAppxEncryptedPackageWriter interface [App packaging and management], IAppxEncryptedPackageWriter interface [App packaging and management],described, appxpackaging/IAppxEncryptedPackageWriter, appxpkg.iappxencryptedpackagewriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxEncryptedPackageWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptedPackageWriter interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Provides a write-only object model for encrypted app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptedPackageWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxEncryptedPackageWriter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4F5823D3-7039-4CA1-BEEA-DF2A13BC54BD">AddPayloadFileEncrypted</a>
</td>
<td align="left" width="63%">
Adds a new encrypted payload file to the appx package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/364F643B-23A2-4E5D-8239-54C8C2052C49">Close</a>
</td>
<td align="left" width="63%">
Closes and finalizes the written package stream.

</td>
</tr>
</table> 

