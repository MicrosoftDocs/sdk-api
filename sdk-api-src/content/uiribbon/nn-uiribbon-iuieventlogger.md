---
UID: NN:uiribbon.IUIEventLogger
title: IUIEventLogger (uiribbon.h)
description: The IUIEventLogger interface is implemented by the application and defines the ribbon events callback method.
helpviewer_keywords: ["IUIEventLogger","IUIEventLogger interface [Windows Ribbon]","IUIEventLogger interface [Windows Ribbon]","described","uiribbon/IUIEventLogger","windowsribbon.iuieventlogger"]
old-location: windowsribbon\iuieventlogger.htm
tech.root: windowsribbon
ms.assetid: 54DB1BFF-0657-4027-8C8C-89CE998253F4
ms.date: 12/05/2018
ms.keywords: IUIEventLogger, IUIEventLogger interface [Windows Ribbon], IUIEventLogger interface [Windows Ribbon],described, uiribbon/IUIEventLogger, windowsribbon.iuieventlogger
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIEventLogger
 - uiribbon/IUIEventLogger
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUIEventLogger
---

# IUIEventLogger interface


## -description

The <b>IUIEventLogger</b> interface is implemented by the 
				application and defines the ribbon events callback method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIEventLogger</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIEventLogger</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIEventLogger</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuieventlogger-onuievent">OnUIEvent</a>
</td>
<td align="left" width="63%">
Receives notifications that a ribbon event has occurred.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuieventingmanager">IUIEventingManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-reference-interfaces">Interfaces</a>

