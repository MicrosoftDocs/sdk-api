---
UID: NN:uianimation.IUIAnimationManagerEventHandler2
title: IUIAnimationManagerEventHandler2 (uianimation.h)
description: Defines a method for handling updates to an animation manager.
helpviewer_keywords: ["IUIAnimationManagerEventHandler2","IUIAnimationManagerEventHandler2 interface [Windows Animation]","IUIAnimationManagerEventHandler2 interface [Windows Animation]","described","uianimation.iuianimationmanagereventhandler2","uianimation/IUIAnimationManagerEventHandler2"]
old-location: uianimation\iuianimationmanagereventhandler2.htm
tech.root: UIAnimation
ms.assetid: 3D3DAC6C-6904-4962-BB17-18FA97678834
ms.date: 12/05/2018
ms.keywords: IUIAnimationManagerEventHandler2, IUIAnimationManagerEventHandler2 interface [Windows Animation], IUIAnimationManagerEventHandler2 interface [Windows Animation],described, uianimation.iuianimationmanagereventhandler2, uianimation/IUIAnimationManagerEventHandler2
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationManagerEventHandler2
 - uianimation/IUIAnimationManagerEventHandler2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationManagerEventHandler2
---

# IUIAnimationManagerEventHandler2 interface


## -description

Defines a method for handling updates to an <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">animation manager</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationManagerEventHandler2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationManagerEventHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationManagerEventHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanagereventhandler2-onmanagerstatuschanged">IUIAnimationManager2::OnManagerStatusChanged</a>
</td>
<td align="left" width="63%">
Handles status changes to an <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">animation manager</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>