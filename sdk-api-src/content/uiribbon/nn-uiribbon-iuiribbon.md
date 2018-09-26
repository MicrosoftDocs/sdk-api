---
UID: NN:uiribbon.IUIRibbon
title: IUIRibbon
author: windows-sdk-content
description: The IUIRibbon interface is implemented by the Windows Ribbon framework and provides the ability to specify settings and properties for a ribbon.
old-location: windowsribbon\windowsribbon_iuiribbon.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\iuiribbon.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIRibbon, IUIRibbon interface [Windows Ribbon], IUIRibbon interface [Windows Ribbon],described, scenicintent_IUIRibbon, uiribbon/IUIRibbon, windowsribbon.windowsribbon_iuiribbon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIRibbon interface


## -description


The <b>IUIRibbon</b> interface is implemented by the Windows Ribbon 
				framework and provides the ability to specify settings and properties for a ribbon. 
			
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIRibbon</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIRibbon</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd742708(v=VS.85).aspx">GetHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the ribbon.		
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd371361(v=VS.85).aspx">LoadSettingsFromStream</a>
</td>
<td align="left" width="63%">
Reads ribbon settings from a binary stream.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd371362(v=VS.85).aspx">SaveSettingsToStream</a>
</td>
<td align="left" width="63%">
Writes ribbon settings to a binary stream.
		

</td>
</tr>
</table> 


## -remarks



A Ribbon is composed of several components that can include an <a href="https://msdn.microsoft.com/en-us/library/Dd940489(v=VS.85).aspx">Application Menu</a>, the <a href="https://msdn.microsoft.com/en-us/library/Dd940502(v=VS.85).aspx">Quick Access Toolbar (QAT)</a>, 
				<a href="https://msdn.microsoft.com/en-us/library/Dd940507(v=VS.85).aspx">Tabs</a> (core and contextual), <a href="https://msdn.microsoft.com/en-us/library/Dd940499(v=VS.85).aspx">Groups</a> (containers for controls), and a rich context menu  system (<a href="https://msdn.microsoft.com/en-us/library/Dd940493(v=VS.85).aspx">Context Popup</a>).
			




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

