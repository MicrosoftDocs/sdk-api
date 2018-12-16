---
UID: NF:uiautomationclient.IUIAutomation.VariantToRect
title: IUIAutomation::VariantToRect
author: windows-sdk-content
description: Converts a VARIANT containing rectangle coordinates to a RECT.
old-location: winauto\uiauto_IUIAutomation_VariantToRect.htm
tech.root: WinAuto
ms.assetid: ef8bb8eb-c6f1-4797-b64f-f4f9d41db2bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],VariantToRect method, IUIAutomation.VariantToRect, IUIAutomation::VariantToRect, VariantToRect, VariantToRect method [Windows Accessibility], VariantToRect method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_VariantToRect, uiauto_IUIAutomation_VariantToRect, uiautomationclient/IUIAutomation::VariantToRect, winauto.uiauto_IUIAutomation_VariantToRect
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
 - IUIAutomation.VariantToRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::VariantToRect


## -description


Converts a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a> containing rectangle coordinates to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>.


## -parameters




### -param var [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a></b>

The coordinates of a rectangle.


### -param rc [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Receives the converted rectangle coordinates.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



