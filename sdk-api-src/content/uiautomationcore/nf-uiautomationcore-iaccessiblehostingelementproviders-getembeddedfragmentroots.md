---
UID: NF:uiautomationcore.IAccessibleHostingElementProviders.GetEmbeddedFragmentRoots
title: IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots
author: windows-sdk-content
description: Retrieves the Microsoft Active Accessibility providers of all windowless Microsoft ActiveX controls that have a Microsoft UI Automation provider implementation, and are hosted in a Microsoft Active Accessibility object that implements the IAccessibleHostingElementProviders interface.
old-location: winauto\uiauto_IAccessibleHostingElementProviders_GetEmbeddedFragmentRoots.htm
old-project: WinAuto
ms.assetid: 39A9665F-C2F3-48A2-A165-50AD3B82455F
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetEmbeddedFragmentRoots, GetEmbeddedFragmentRoots method [Windows Accessibility], GetEmbeddedFragmentRoots method [Windows Accessibility],IAccessibleHostingElementProviders interface, IAccessibleHostingElementProviders interface [Windows Accessibility],GetEmbeddedFragmentRoots method, IAccessibleHostingElementProviders.GetEmbeddedFragmentRoots, IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots, uiautomationcore/IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots, winauto.uiauto_IAccessibleHostingElementProviders_GetEmbeddedFragmentRoots
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.h
api_name:
-	IAccessibleHostingElementProviders.GetEmbeddedFragmentRoots
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots


## -description


Retrieves the  Microsoft Active Accessibility providers of  all windowless Microsoft ActiveX controls that have a Microsoft UI Automation provider implementation, and are hosted in a Microsoft Active Accessibility object that implements the <a href="https://msdn.microsoft.com/8D974311-25CB-4D49-B907-2984D0DA58D7">IAccessibleHostingElementProviders</a> interface.


## -parameters




### -param pRetVal [out, retval]

Type: <b>SAFEARRAY**</b>

Receives the <a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a> interface pointers.  


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The container of windowless ActiveX controls implements this method on the same object that implements the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface.  When called, this method queries each of the contained windowless ActiveX controls for an <a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a> pointer, and then adds the pointer to the safe array.  

This method should not include any providers that do not implement <b>IRawElementProviderFragmentRoot</b>. 





## -see-also




<a href="https://msdn.microsoft.com/8D974311-25CB-4D49-B907-2984D0DA58D7">IAccessibleHostingElementProviders</a>
 

 

