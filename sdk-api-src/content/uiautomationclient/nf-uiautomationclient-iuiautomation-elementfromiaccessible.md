---
UID: NF:uiautomationclient.IUIAutomation.ElementFromIAccessible
title: IUIAutomation::ElementFromIAccessible
author: windows-sdk-content
description: Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server.
old-location: winauto\uiauto_IUIAutomation_ElementFromIAccessible.htm
tech.root: WinAuto
ms.assetid: b3dcc31c-e111-4841-82a8-a6329020b595
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ElementFromIAccessible, ElementFromIAccessible method [Windows Accessibility], ElementFromIAccessible method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromIAccessible method, IUIAutomation.ElementFromIAccessible, IUIAutomation::ElementFromIAccessible, uiauto.uiauto_IUIAutomation_ElementFromIAccessible, uiauto_IUIAutomation_ElementFromIAccessible, uiautomationclient/IUIAutomation::ElementFromIAccessible, winauto.uiauto_IUIAutomation_ElementFromIAccessible
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - UIAutomationClient.h
api_name:
 - IUIAutomation.ElementFromIAccessible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::ElementFromIAccessible


## -description


Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server.


## -parameters




### -param accessible [in]

Type: <b><a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface of the accessible object.


### -param childId [in]

Type: <b>int</b>

The child ID of the accessible object.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method enables UI Automation clients to get <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interfaces for accessible objects implemented by a Microsoft Active Accessiblity server. 

This method may fail if the server implements UI Automation provider interfaces alongside Microsoft Active Accessibility support. 

The method returns E_INVALIDARG if the underlying implementation of the Microsoft UI Automation element is not a native Microsoft Active Accessibility server; that is, if a client attempts to retrieve the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface for an element originally supported by a proxy object from Oleacc.dll, or by the UIA-to-MSAA Bridge.




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/b6c1e03b-7c0e-4dee-b276-bfc7d6247d4e">IUIAutomation::ElementFromHandleBuildCache</a>
 

 

