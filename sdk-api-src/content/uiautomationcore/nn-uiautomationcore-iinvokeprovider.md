---
UID: NN:uiautomationcore.IInvokeProvider
title: IInvokeProvider (uiautomationcore.h)

description: Provides access to controls that initiate or perform a single, unambiguous action and do not maintain state when activated.
old-location: winauto\uiauto_IInvokeProvider.htm
tech.root: WinAuto
ms.assetid: e522b8d5-c6f6-4f71-a8c8-4332f2824f72

ms.date: 12/05/2018
ms.keywords: IInvokeProvider, IInvokeProvider interface [Windows Accessibility], IInvokeProvider interface [Windows Accessibility],described, uiauto.uiauto_IInvokeProvider, uiauto_IInvokeProvider, uiautomationcore/IInvokeProvider, winauto.uiauto_IInvokeProvider
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/IInvokeProvider"
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
 - IInvokeProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInvokeProvider interface


## -description


Provides access to controls 
        that initiate or perform a single, unambiguous action and do not maintain state when activated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInvokeProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInvokeProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInvokeProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iinvokeprovider-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Sends a request to activate a control and initiate its single, unambiguous action.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must 
        support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementinginvoke">Invoke</a> control pattern.
		

Controls implement <b>IInvokeProvider</b> if the same behavior is not 
        exposed through another  control pattern provider. For example, if 
        the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iinvokeprovider-invoke">Invoke</a> method of a control performs the same 
        action as the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iexpandcollapseprovider-expand">IExpandCollapseProvider::Expand</a> or <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iexpandcollapseprovider-collapse">Collapse</a> 
        method, the control should not also implement <b>IInvokeProvider</b>.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

