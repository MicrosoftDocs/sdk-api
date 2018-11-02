---
UID: NF:uiautomationclient.IUIAutomation.RectToVariant
title: IUIAutomation::RectToVariant
author: windows-sdk-content
description: Creates a VARIANT that contains the coordinates of a rectangle.
old-location: winauto\uiauto_IUIAutomation_RectToVariant.htm
tech.root: WinAuto
ms.assetid: abfb2bb1-7594-4f32-9188-05745006ae18
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],RectToVariant method, IUIAutomation.RectToVariant, IUIAutomation::RectToVariant, RectToVariant, RectToVariant method [Windows Accessibility], RectToVariant method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_RectToVariant, uiauto_IUIAutomation_RectToVariant, uiautomationclient/IUIAutomation::RectToVariant, winauto.uiauto_IUIAutomation_RectToVariant
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
 - IUIAutomation.RectToVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::RectToVariant


## -description


Creates a <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a> that contains the coordinates of a rectangle.


## -parameters




### -param rc [in]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a structure that contains the coordinates of the rectangle.


### -param var [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a>*</b>

Receives the coordinates of the rectangle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a> has a data type of VT_ARRAY | VT_R8.
			




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/ef8bb8eb-c6f1-4797-b64f-f4f9d41db2bb">IUIAutomation::VariantToRect</a>
 

 

