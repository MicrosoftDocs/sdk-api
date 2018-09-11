---
UID: NF:uiautomationclient.IUIAutomation.CheckNotSupported
title: IUIAutomation::CheckNotSupported
author: windows-sdk-content
description: Checks a provided VARIANT to see if it contains the Not Supported identifier.
old-location: winauto\uiauto_IUIAutomation_CheckNotSupported.htm
tech.root: WinAuto
ms.assetid: c7fd7d1e-3f7b-4700-9263-2cab6e0de896
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CheckNotSupported, CheckNotSupported method [Windows Accessibility], CheckNotSupported method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CheckNotSupported method, IUIAutomation.CheckNotSupported, IUIAutomation::CheckNotSupported, uiauto.uiauto_IUIAutomation_CheckNotSupported, uiauto_IUIAutomation_CheckNotSupported, uiautomationclient/IUIAutomation::CheckNotSupported, winauto.uiauto_IUIAutomation_CheckNotSupported
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
 - IUIAutomation.CheckNotSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::CheckNotSupported


## -description


Checks a provided <a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> to see if it contains the Not Supported identifier.


## -parameters




### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a></b>

The value to check.


### -param isNotSupported [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Receives <b>TRUE</b> if the provided <a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> contains the Not Supported identifier, or <b>FALSE</b> otherwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After retrieving a property for a UI Automation element, call this method to determine whether the element supports the retrieved property. <b>CheckNotSupported</b> is typically called after calling a property retrieving method such as <a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">GetCurrentPropertyValue</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/00162b3c-fab8-4559-83c0-d8c6731441c3">IUIAutomation::ReservedNotSupportedValue</a>
 

 

