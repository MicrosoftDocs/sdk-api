---
UID: NF:uiautomationcore.IRawElementProviderHostingAccessibles.GetEmbeddedAccessibles
title: IRawElementProviderHostingAccessibles::GetEmbeddedAccessibles (uiautomationcore.h)
author: windows-sdk-content
description: Retrieves the IAccessible interface pointers of the windowless Microsoft ActiveX controls that are hosted by this provider.
old-location: winauto\uiauto_IRawElementProviderHostingAccessibles_GetEmbeddedAccessibles.htm
tech.root: WinAuto
ms.assetid: E428B87C-25FE-437B-AAE8-7E3BC79BBE6B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEmbeddedAccessibles, GetEmbeddedAccessibles method [Windows Accessibility], GetEmbeddedAccessibles method [Windows Accessibility],IRawElementProviderHostingAccessibles interface, IRawElementProviderHostingAccessibles interface [Windows Accessibility],GetEmbeddedAccessibles method, IRawElementProviderHostingAccessibles.GetEmbeddedAccessibles, IRawElementProviderHostingAccessibles::GetEmbeddedAccessibles, uiautomationcore/IRawElementProviderHostingAccessibles::GetEmbeddedAccessibles, winauto.uiauto_IRawElementProviderHostingAccessibles_GetEmbeddedAccessibles
ms.topic: method
f1_keywords: 
 - "uiautomationcore/IRawElementProviderHostingAccessibles.GetEmbeddedAccessibles"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderHostingAccessibles.GetEmbeddedAccessibles
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRawElementProviderHostingAccessibles::GetEmbeddedAccessibles


## -description


Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointers of the windowless Microsoft ActiveX controls that are hosted by this provider.   


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives the <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> pointers of the hosted windowless ActiveX controls.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An ActiveX control container with an existing <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a> interface implements this method on the same object that implements <b>IRawElementProviderFragmentRoot</b>.  When called, this method should query each contained windowless control for an <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> pointer and then add the pointer  to the safe array.  



This method should ignore providers that do not implement <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>.  




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles">IRawElementProviderHostingAccessibles</a>
 

 

