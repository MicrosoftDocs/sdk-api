---
UID: NN:appxpackaging.IAppxEncryptedBundleWriter
title: IAppxEncryptedBundleWriter
author: windows-sdk-content
description: Provides a write-only object model for encrypted bundle packages.
old-location: appxpkg\iappxencryptedbundlewriter.htm
tech.root: appxpkg
ms.assetid: E88355DA-F7BE-45C7-9DDB-EC39DB2AD280
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAppxEncryptedBundleWriter, IAppxEncryptedBundleWriter interface [App packaging and management], IAppxEncryptedBundleWriter interface [App packaging and management],described, appxpackaging/IAppxEncryptedBundleWriter, appxpkg.iappxencryptedbundlewriter
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAppxEncryptedBundleWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxEncryptedBundleWriter interface


## -description


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
<a href="https://msdn.microsoft.com/0ED396CC-3CDA-440A-9FA7-3F3A85522778">Close</a>
</td>
<td align="left" width="63%">
Writes the bundle manifest and blockmap footprint files to the bundle.

</td>
</tr>
</table> 

