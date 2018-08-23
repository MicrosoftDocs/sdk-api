---
UID: NN:appxpackaging.IAppxBundleWriter
title: IAppxBundleWriter
author: windows-sdk-content
description: Provides a write-only object model for bundle packages.
old-location: appxpkg\iappxbundlewriter.htm
old-project: appxpkg
ms.assetid: 5762E634-CBA6-496C-A771-CA5718E7E6AD
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: IAppxBundleWriter, IAppxBundleWriter interface [App packaging and management], IAppxBundleWriter interface [App packaging and management],described, appxpackaging/IAppxBundleWriter, appxpkg.iappxbundlewriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleWriter interface


## -description


Provides a write-only object model for bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4772621D-2A8E-439B-8AD7-01A5BD31002B">AddPayloadPackage</a>
</td>
<td align="left" width="63%">
Adds a new app package to the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9826873D-87AF-4D6B-977B-1C24197C47F8">Close</a>
</td>
<td align="left" width="63%">
Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.

</td>
</tr>
</table> 


## -remarks



You can use the <a href="https://msdn.microsoft.com/E77392FB-69A1-41B0-8B44-F05F126214E0">CreateBundleWriter</a> method of the <a href="https://msdn.microsoft.com/33A320BD-7B68-4C42-A776-25CC744C6652">IAppxBundleFactory</a> interface to retrieve the <b>IAppxBundleWriter</b> object. 

You can add only app packages to the writer.  The writer automatically generates footprint files, such as, the bundle’s manifest and block map.



