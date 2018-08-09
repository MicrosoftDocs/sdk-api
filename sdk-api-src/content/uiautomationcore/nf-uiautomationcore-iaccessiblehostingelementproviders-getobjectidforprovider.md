---
UID: NF:uiautomationcore.IAccessibleHostingElementProviders.GetObjectIdForProvider
title: IAccessibleHostingElementProviders::GetObjectIdForProvider
author: windows-sdk-content
description: Retrieves the object ID associated with a contained windowless Microsoft ActiveX control that implements Microsoft UI Automation.
old-location: winauto\uiauto_IAccessibleHostingElementProviders_GetObjectIdForProvider.htm
old-project: WinAuto
ms.assetid: 847F285F-F31D-486C-BBC7-DEED69505306
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetObjectIdForProvider, GetObjectIdForProvider method [Windows Accessibility], GetObjectIdForProvider method [Windows Accessibility],IAccessibleHostingElementProviders interface, IAccessibleHostingElementProviders interface [Windows Accessibility],GetObjectIdForProvider method, IAccessibleHostingElementProviders.GetObjectIdForProvider, IAccessibleHostingElementProviders::GetObjectIdForProvider, uiautomationcore/IAccessibleHostingElementProviders::GetObjectIdForProvider, winauto.uiauto_IAccessibleHostingElementProviders_GetObjectIdForProvider
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
 - IAccessibleHostingElementProviders.GetObjectIdForProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAccessibleHostingElementProviders::GetObjectIdForProvider


## -description


Retrieves the object ID associated with a contained windowless Microsoft ActiveX control that implements Microsoft UI Automation.  


## -parameters




### -param pProvider [in, optional]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider for the windowless ActiveX control.


### -param pidObject [out]

Type: <b>long*</b>

The object ID of the contained windowless ActiveX control.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8D974311-25CB-4D49-B907-2984D0DA58D7">IAccessibleHostingElementProviders</a>
 

 

