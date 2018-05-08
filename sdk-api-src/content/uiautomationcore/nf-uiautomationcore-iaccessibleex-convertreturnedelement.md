---
UID: NF:uiautomationcore.IAccessibleEx.ConvertReturnedElement
title: IAccessibleEx::ConvertReturnedElement
author: windows-driver-content
description: Retrieves the IAccessibleEx interface of an element returned as a property value.
old-location: winauto\uiauto_IAccessibleEx_ConvertReturnedElement.htm
old-project: WinAuto
ms.assetid: eafda7ed-b18c-4d52-9d1c-a9d1a2d5dfd1
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ConvertReturnedElement, ConvertReturnedElement method [Windows Accessibility], ConvertReturnedElement method [Windows Accessibility],IAccessibleEx interface, IAccessibleEx interface [Windows Accessibility],ConvertReturnedElement method, IAccessibleEx.ConvertReturnedElement, IAccessibleEx::ConvertReturnedElement, uiauto.uiauto_IAccessibleEx_ConvertReturnedElement, uiauto_IAccessibleEx_ConvertReturnedElement, uiautomationcore/IAccessibleEx::ConvertReturnedElement, winauto.uiauto_IAccessibleEx_ConvertReturnedElement
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
-	UIAutomationCore.h
api_name:
-	IAccessibleEx.ConvertReturnedElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAccessibleEx::ConvertReturnedElement


## -description


Retrieves the <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> interface of an element returned as a property value.


## -parameters




### -param pIn [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interface that was retrieved as a property.


### -param ppRetValOut [out]

Type: <b><a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a>**</b>

Receives a pointer to the <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a>  interface of the element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the bridge between Microsoft UI Automation and Microsoft Active Accessibility. Most other implementations should return E_NOTIMPL after setting <i>ppRetValOut</i> to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a>
 

 

