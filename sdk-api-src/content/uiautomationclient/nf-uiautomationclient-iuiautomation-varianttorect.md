---
UID: NF:uiautomationclient.IUIAutomation.VariantToRect
title: IUIAutomation::VariantToRect (uiautomationclient.h)
author: windows-sdk-content
description: Converts a VARIANT containing rectangle coordinates to a RECT.
old-location: winauto\uiauto_IUIAutomation_VariantToRect.htm
tech.root: WinAuto
ms.assetid: ef8bb8eb-c6f1-4797-b64f-f4f9d41db2bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],VariantToRect method, IUIAutomation.VariantToRect, IUIAutomation::VariantToRect, VariantToRect, VariantToRect method [Windows Accessibility], VariantToRect method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_VariantToRect, uiauto_IUIAutomation_VariantToRect, uiautomationclient/IUIAutomation::VariantToRect, winauto.uiauto_IUIAutomation_VariantToRect
ms.topic: method
f1_keywords: 
 - "uiautomationclient/IUIAutomation.VariantToRect"
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
ms.custom: 19H1
---

# IUIAutomation::VariantToRect


## -description


Converts a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> containing rectangle coordinates to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>.


## -parameters




### -param var [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a></b>

The coordinates of a rectangle.


### -param rc [out, retval]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Receives the converted rectangle coordinates.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



