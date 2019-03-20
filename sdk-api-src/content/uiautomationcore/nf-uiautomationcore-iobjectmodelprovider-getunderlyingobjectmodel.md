---
UID: NF:uiautomationcore.IObjectModelProvider.GetUnderlyingObjectModel
title: IObjectModelProvider::GetUnderlyingObjectModel (uiautomationcore.h)
author: windows-sdk-content
description: Retrieves an interface used to access the underlying object model of the provider.
old-location: winauto\uiauto_IObjectModelProvider_GetUnderlyingObjectModel.htm
tech.root: WinAuto
ms.assetid: 305758A1-D584-45A3-B118-B46B3731820D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUnderlyingObjectModel, GetUnderlyingObjectModel method [Windows Accessibility], GetUnderlyingObjectModel method [Windows Accessibility],IObjectModelProvider interface, IObjectModelProvider interface [Windows Accessibility],GetUnderlyingObjectModel method, IObjectModelProvider.GetUnderlyingObjectModel, IObjectModelProvider::GetUnderlyingObjectModel, uiautomationcore/IObjectModelProvider::GetUnderlyingObjectModel, winauto.uiauto_IObjectModelProvider_GetUnderlyingObjectModel
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
 - IObjectModelProvider.GetUnderlyingObjectModel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectModelProvider::GetUnderlyingObjectModel


## -description


Retrieves an interface used to access the underlying object model of the provider.


## -parameters




### -param ppUnknown [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives an interface for accessing the underlying object model.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Client applications can use the object model to directly access the content of the control or application.




## -see-also




<a href="https://msdn.microsoft.com/E374F95B-9F0A-41D6-A916-F5CD5F5E442D">IObjectModelProvider</a>
 

 

