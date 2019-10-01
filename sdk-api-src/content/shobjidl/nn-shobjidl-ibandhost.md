---
UID: NN:shobjidl.IBandHost
title: IBandHost (shobjidl.h)
author: windows-sdk-content
description: Exposes methods that create and destroy bands and specifiy their availability.
old-location: shell\IBandHost.htm
tech.root: shell
ms.assetid: 8d9fe92a-812e-4fa0-954b-37aa48b52008
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBandHost, IBandHost interface [Windows Shell], IBandHost interface [Windows Shell],described, _shell_IBandHost, shell.IBandHost, shobjidl/IBandHost
ms.topic: interface
f1_keywords: 
 - "shobjidl/IBandHost"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBandHost interface


## -description


Exposes methods that create and destroy bands and specifiy their availability.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBandHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBandHost</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ibandhost-createband">CreateBand</a>
</td>
<td align="left" width="63%">
Creates a specified band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ibandhost-destroyband">DestroyBand</a>
</td>
<td align="left" width="63%">
Destroys a specified band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ibandhost-setbandavailability">SetBandAvailability</a>
</td>
<td align="left" width="63%">
Sets the availability of a specified band.

</td>
</tr>
</table> 

