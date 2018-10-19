---
UID: NN:shobjidl.IBandHost
title: IBandHost
author: windows-sdk-content
description: Exposes methods that create and destroy bands and specifiy their availability.
old-location: shell\IBandHost.htm
tech.root: shell
ms.assetid: 8d9fe92a-812e-4fa0-954b-37aa48b52008
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IBandHost, IBandHost interface [Windows Shell], IBandHost interface [Windows Shell],described, _shell_IBandHost, shell.IBandHost, shobjidl/IBandHost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl.h
api_name:
 - IBandHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBandHost interface


## -description


Exposes methods that create and destroy bands and specifiy their availability.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBandHost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBandHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBandHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7edf8d46-f925-4c4f-99b1-e792dce69222">CreateBand</a>
</td>
<td align="left" width="63%">
Creates a specified band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc9fec01-97ff-44d9-833a-cd781977e5b9">DestroyBand</a>
</td>
<td align="left" width="63%">
Destroys a specified band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3e41e8f-45dd-4160-8a65-ec82b7e9abe7">SetBandAvailability</a>
</td>
<td align="left" width="63%">
Sets the availability of a specified band.

</td>
</tr>
</table> 

