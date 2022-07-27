---
UID: NF:uiautomationcore.ITextEditProvider.GetActiveComposition
title: ITextEditProvider::GetActiveComposition (uiautomationcore.h)
description: Returns the active composition. (ITextEditProvider.GetActiveComposition)
helpviewer_keywords: ["GetActiveComposition","GetActiveComposition method [Windows Accessibility]","GetActiveComposition method [Windows Accessibility]","ITextEditProvider interface","ITextEditProvider interface [Windows Accessibility]","GetActiveComposition method","ITextEditProvider.GetActiveComposition","ITextEditProvider::GetActiveComposition","uiautomationcore/ITextEditProvider::GetActiveComposition","winauto.uiauto_ITextEditProvider_GetActiveComposition"]
old-location: winauto\uiauto_ITextEditProvider_GetActiveComposition.htm
tech.root: WinAuto
ms.assetid: E0A4E340-8F23-8EE0-31E4-90DB8D8E68FF
ms.date: 12/05/2018
ms.keywords: GetActiveComposition, GetActiveComposition method [Windows Accessibility], GetActiveComposition method [Windows Accessibility],ITextEditProvider interface, ITextEditProvider interface [Windows Accessibility],GetActiveComposition method, ITextEditProvider.GetActiveComposition, ITextEditProvider::GetActiveComposition, uiautomationcore/ITextEditProvider::GetActiveComposition, winauto.uiauto_ITextEditProvider_GetActiveComposition
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextEditProvider::GetActiveComposition
 - uiautomationcore/ITextEditProvider::GetActiveComposition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextEditProvider.GetActiveComposition
---

# ITextEditProvider::GetActiveComposition


## -description

Returns the active composition.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Pointer to the range of the current conversion (none if there is no conversion).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Follow the guidance given in <a href="/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a> that describes how to implement this method and how to raise the related notification events.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider">ITextEditProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>



<a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent">UiaRaiseTextEditTextChangedEvent</a>
