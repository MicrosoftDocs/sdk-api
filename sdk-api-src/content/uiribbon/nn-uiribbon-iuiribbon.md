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
f1_keywords:
- uiribbon/IUIRibbon
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uiribbon.dll
api_name:
- IUIRibbon
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIRibbon interface


## -description


The <b>IUIRibbon</b> interface is implemented by the Windows Ribbon 
				framework and provides the ability to specify settings and properties for a ribbon. 
			
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIRibbon</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIRibbon</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIRibbon</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight">GetHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the ribbon.		
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream">LoadSettingsFromStream</a>
</td>
<td align="left" width="63%">
Reads ribbon settings from a binary stream.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream">SaveSettingsToStream</a>
</td>
<td align="left" width="63%">
Writes ribbon settings to a binary stream.
		

</td>
</tr>
</table> 


## -remarks



A Ribbon is composed of several components that can include an <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-controls-applicationmenu">Application Menu</a>, the <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-controls-quickaccesstoolbar">Quick Access Toolbar (QAT)</a>, 
				<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-controls-tab">Tabs</a> (core and contextual), <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-controls-group">Groups</a> (containers for controls), and a rich context menu  system (<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a>).
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
 

 

