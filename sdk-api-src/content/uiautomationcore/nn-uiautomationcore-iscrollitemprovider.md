---
UID: NN:uiautomationcore.IScrollItemProvider
title: IScrollItemProvider (uiautomationcore.h)
description: Provides access to individual child controls of containers that implement IScrollProvider.
old-location: winauto\uiauto_IScrollItemProvider.htm
tech.root: WinAuto
ms.assetid: d8a8384e-d57b-4614-a643-b5ba3a63224d
ms.date: 12/05/2018
ms.keywords: IScrollItemProvider, IScrollItemProvider interface [Windows Accessibility], IScrollItemProvider interface [Windows Accessibility],described, uiauto.uiauto_IScrollItemProvider, uiauto_IScrollItemProvider, uiautomationcore/IScrollItemProvider, winauto.uiauto_IScrollItemProvider
f1_keywords:
- uiautomationcore/IScrollItemProvider
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IScrollItemProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IScrollItemProvider interface


## -description


Provides access 
        to individual child controls of containers that implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iscrollprovider">IScrollProvider</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScrollItemProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IScrollItemProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IScrollItemProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollitemprovider-scrollintoview">ScrollIntoView</a>
</td>
<td align="left" width="63%">
Scrolls the content area of a container object in order to display the control within the visible region (viewport) of the container.
        

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must 
            support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingscrollitem">ScrollItem</a> control pattern.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

