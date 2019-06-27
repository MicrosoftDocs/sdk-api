---
UID: NN:thumbcache.IThumbnailSettings
title: IThumbnailSettings (thumbcache.h)
author: windows-sdk-content
description: Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request.
old-location: shell\IThumbnailSettings.htm
tech.root: shell
ms.assetid: 502537E5-1D72-44f0-BC75-DBED61F174FC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IThumbnailSettings, IThumbnailSettings interface [Windows Shell], IThumbnailSettings interface [Windows Shell],described, shell.IThumbnailSettings, thumbcache/IThumbnailSettings
ms.topic: interface
f1_keywords: 
 - "thumbcache/IThumbnailSettings"
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
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
 - Thumbcache.h
api_name:
 - IThumbnailSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IThumbnailSettings interface


## -description


Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThumbnailSettings</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IThumbnailSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IThumbnailSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailsettings-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Enables a thumbnail provider to return a thumbnail specific to the user's context.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
This interface can be implemented by any thumbnail provider that supports <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a> or <a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailprovider">IThumbnailProvider</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

