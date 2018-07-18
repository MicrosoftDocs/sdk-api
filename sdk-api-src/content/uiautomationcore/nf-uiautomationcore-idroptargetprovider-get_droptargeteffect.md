---
UID: NF:uiautomationcore.IDropTargetProvider.get_DropTargetEffect
title: IDropTargetProvider::get_DropTargetEffect
author: windows-sdk-content
description: Retrieves a localized string that describes the effect that happens when the user drops the grabbed element on this drop target.
old-location: winauto\uiauto_idroptargetprovider_droptargeteffect.htm
old-project: WinAuto
ms.assetid: F94D0513-543D-4B9D-A665-2197349C3B55
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: DropTargetEffect property [Windows Accessibility], DropTargetEffect property [Windows Accessibility],IDropTargetProvider interface, IDropTargetProvider interface [Windows Accessibility],DropTargetEffect property, IDropTargetProvider.DropTargetEffect, IDropTargetProvider.get_DropTargetEffect, IDropTargetProvider::DropTargetEffect, IDropTargetProvider::get_DropTargetEffect, get_DropTargetEffect, uiautomationcore/IDropTargetProvider::DropTargetEffect, uiautomationcore/IDropTargetProvider::get_DropTargetEffect, winauto.uiauto_idroptargetprovider_droptargeteffect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IDropTargetProvider.DropTargetEffect
 - IDropTargetProvider.get_DropTargetEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDropTargetProvider::get_DropTargetEffect


## -description


Retrieves a localized string that describes the effect that happens when the user drops the grabbed element on this drop target.

This property is read-only.


## -parameters


## -remarks



This property describes the default effect that happens when the user drops a grabbed element on a target, such as moving or copying the element.  This property can be a short string such as "move", or a longer one such as "insert into Main group".  The string is always localized.

If this property changes, the provider must notify clients by firing a <a href="uiauto_event_ids.htm">UIA_AutomationPropertyChangedEventId</a> event. 



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IFACEMETHODIMP CRegionProvider::get_DropTargetEffect(BSTR * pDefaultDropAction)
{
    WCHAR wszDropAction[100];
    LoadString(g_hInstance, IDS_REGION_DEFAULTDROPACTION1, wszDropAction, 
        ARRAYSIZE(wszDropAction));
    *pDefaultDropAction = ::SysAllocString(wszDropAction);
    return (*pDefaultDropAction == nullptr) ? E_OUTOFMEMORY : S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ECCDC429-4829-46E0-AE77-270024E2DA48">IDropTargetProvider</a>
 

 

