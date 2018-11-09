---
UID: NF:uiautomationclient.IUIAutomationObjectModelPattern.GetUnderlyingObjectModel
title: IUIAutomationObjectModelPattern::GetUnderlyingObjectModel
author: windows-sdk-content
description: Retrieves an interface used to access the underlying object model of the provider.
old-location: winauto\uiauto_IUIAutomationObjectModelPattern_GetUnderlyingObjectModel.htm
tech.root: WinAuto
ms.assetid: 7D1C4ABD-38FA-48C4-80ED-C0AA312D45FE
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetUnderlyingObjectModel, GetUnderlyingObjectModel method [Windows Accessibility], GetUnderlyingObjectModel method [Windows Accessibility],IUIAutomationObjectModelPattern interface, IUIAutomationObjectModelPattern interface [Windows Accessibility],GetUnderlyingObjectModel method, IUIAutomationObjectModelPattern.GetUnderlyingObjectModel, IUIAutomationObjectModelPattern::GetUnderlyingObjectModel, uiautomationclient/IUIAutomationObjectModelPattern::GetUnderlyingObjectModel, winauto.uiauto_IUIAutomationObjectModelPattern_GetUnderlyingObjectModel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUIAutomationObjectModelPattern.GetUnderlyingObjectModel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationObjectModelPattern::GetUnderlyingObjectModel


## -description


Retrieves an interface used to access the underlying object model of the provider.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives an interface for accessing the underlying object model.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Client applications can use the object model to directly access the content of the control or application.




## -see-also




<a href="https://msdn.microsoft.com/044A1EE7-4CBD-45E3-A1A8-CA00DC03E136">IUIAutomationObjectModelPattern</a>
 

 

