---
UID: NN:shobjidl_core.IPreviewHandlerVisuals
title: IPreviewHandlerVisuals (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods for applying color and font information to preview handlers.
old-location: shell\IPreviewHandlerVisuals.htm
tech.root: shell
ms.assetid: 3e07af46-4271-472d-be80-70eccc26729c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPreviewHandlerVisuals, IPreviewHandlerVisuals interface [Windows Shell], IPreviewHandlerVisuals interface [Windows Shell],described, _shell_IPreviewHandlerVisuals, shell.IPreviewHandlerVisuals, shobjidl_core/IPreviewHandlerVisuals
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IPreviewHandlerVisuals"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - shobjidl_core.h
api_name:
 - IPreviewHandlerVisuals
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
---

# IPreviewHandlerVisuals interface


## -description


Exposes methods for applying color and font information to preview handlers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPreviewHandlerVisuals</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPreviewHandlerVisuals</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPreviewHandlerVisuals</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlervisuals-setbackgroundcolor">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the background color of the preview handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlervisuals-setfont">SetFont</a>
</td>
<td align="left" width="63%">
Sets the font attributes to be used for text within the preview handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlervisuals-settextcolor">SetTextColor</a>
</td>
<td align="left" width="63%">
Sets the color of the text within the preview handler.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  These are suggestions. It is not compulsory for this interface to be called. The preview handlers must be able to make their own decisions.</div>
<div> </div>


