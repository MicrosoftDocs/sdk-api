---
UID: NN:appxpackaging.IAppxEncryptedBundleWriter
title: IAppxEncryptedBundleWriter
author: windows-sdk-content
description: Provides a write-only object model for encrypted bundle packages.
old-location: appxpkg\iappxencryptedbundlewriter.htm
old-project: appxpkg
ms.assetid: E88355DA-F7BE-45C7-9DDB-EC39DB2AD280
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxEncryptedBundleWriter, IAppxEncryptedBundleWriter interface [App packaging and management], IAppxEncryptedBundleWriter interface [App packaging and management],described, appxpackaging/IAppxEncryptedBundleWriter, appxpkg.iappxencryptedbundlewriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IAppxEncryptedBundleWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptedBundleWriter interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Provides a write-only object model for encrypted bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptedBundleWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxEncryptedBundleWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptedBundleWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/974C29A7-3FEE-4042-986F-D8FD3774F9A6">AddPayloadPackageEncrypted</a>
</td>
<td align="left" width="63%">
Encrypts a new payload package to the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Writes the bundle manifest and blockmap footprint files to the bundle.

</td>
</tr>
</table> 

