---
UID: NN:uiribbon.IUIRibbon
title: IUIRibbon (uiribbon.h)
description: The IUIRibbon interface is implemented by the Windows Ribbon framework and provides the ability to specify settings and properties for a ribbon.
helpviewer_keywords: ["IUIRibbon","IUIRibbon interface [Windows Ribbon]","IUIRibbon interface [Windows Ribbon]","described","scenicintent_IUIRibbon","uiribbon/IUIRibbon","windowsribbon.windowsribbon_iuiribbon"]
old-location: windowsribbon\windowsribbon_iuiribbon.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\iuiribbon.htm
ms.date: 12/05/2018
ms.keywords: IUIRibbon, IUIRibbon interface [Windows Ribbon], IUIRibbon interface [Windows Ribbon],described, scenicintent_IUIRibbon, uiribbon/IUIRibbon, windowsribbon.windowsribbon_iuiribbon
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - IUIRibbon
 - uiribbon/IUIRibbon
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
 - IUIRibbon
---

# IUIRibbon interface


## -description

The <b>IUIRibbon</b> interface is implemented by the Windows Ribbon 
				framework and provides the ability to specify settings and properties for a ribbon.

## -inheritance

The <b>IUIRibbon</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIRibbon</b> also has these types of members:

## -remarks

A Ribbon is composed of several components that can include an <a href="/windows/desktop/windowsribbon/windowsribbon-controls-applicationmenu">Application Menu</a>, the <a href="/windows/desktop/windowsribbon/windowsribbon-controls-quickaccesstoolbar">Quick Access Toolbar (QAT)</a>, 
				<a href="/windows/desktop/windowsribbon/windowsribbon-controls-tab">Tabs</a> (core and contextual), <a href="/windows/desktop/windowsribbon/windowsribbon-controls-group">Groups</a> (containers for controls), and a rich context menu  system (<a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a>).

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
