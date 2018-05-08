---
UID: NF:uiautomationcore.ILegacyIAccessibleProvider.GetIAccessible
title: ILegacyIAccessibleProvider::GetIAccessible
author: windows-driver-content
description: Retrieves an accessible object that corresponds to a UI Automation element that supports the LegacyIAccessible control pattern.
old-location: winauto\uiauto_ILegacyIAccessibleProvider_GetIAccessible.htm
old-project: WinAuto
ms.assetid: 1d156866-d19a-4fd2-8664-d22e8b5434be
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetIAccessible, GetIAccessible method [Windows Accessibility], GetIAccessible method [Windows Accessibility],ILegacyIAccessibleProvider interface, ILegacyIAccessibleProvider interface [Windows Accessibility],GetIAccessible method, ILegacyIAccessibleProvider.GetIAccessible, ILegacyIAccessibleProvider::GetIAccessible, uiauto.uiauto_ILegacyIAccessibleProvider_GetIAccessible, uiauto_ILegacyIAccessibleProvider_GetIAccessible, uiautomationcore/ILegacyIAccessibleProvider::GetIAccessible, winauto.uiauto_ILegacyIAccessibleProvider_GetIAccessible
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
-	Uiautomationcore.dll
api_name:
-	ILegacyIAccessibleProvider.GetIAccessible
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILegacyIAccessibleProvider::GetIAccessible


## -description


Retrieves an accessible object that corresponds to a UI Automation element that supports the <a href="https://msdn.microsoft.com/4d66b9b8-ddbe-4bbc-b475-72dad1fe9393">LegacyIAccessible</a> control pattern.


## -parameters




### -param ppAccessible [out]

Type: <b><a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>**</b>

Receives a pointer to the accessible object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9d911238-05d9-4bba-920f-40ca23ab9549">ILegacyIAccessibleProvider</a>
 

 

