---
UID: NF:uiautomationcore.ITextEditProvider.GetConversionTarget
title: ITextEditProvider::GetConversionTarget (uiautomationcore.h)
description: Returns the current conversion target range. (ITextEditProvider.GetConversionTarget)
helpviewer_keywords: ["GetConversionTarget","GetConversionTarget method [Windows Accessibility]","GetConversionTarget method [Windows Accessibility]","ITextEditProvider interface","ITextEditProvider interface [Windows Accessibility]","GetConversionTarget method","ITextEditProvider.GetConversionTarget","ITextEditProvider::GetConversionTarget","uiautomationcore/ITextEditProvider::GetConversionTarget","winauto.uiauto_ITextEditProvider_GetConversionTarget"]
old-location: winauto\uiauto_ITextEditProvider_GetConversionTarget.htm
tech.root: WinAuto
ms.assetid: C05DC0F6-FB24-2D06-C2D8-43ADF2C110F9
ms.date: 12/05/2018
ms.keywords: GetConversionTarget, GetConversionTarget method [Windows Accessibility], GetConversionTarget method [Windows Accessibility],ITextEditProvider interface, ITextEditProvider interface [Windows Accessibility],GetConversionTarget method, ITextEditProvider.GetConversionTarget, ITextEditProvider::GetConversionTarget, uiautomationcore/ITextEditProvider::GetConversionTarget, winauto.uiauto_ITextEditProvider_GetConversionTarget
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
 - ITextEditProvider::GetConversionTarget
 - uiautomationcore/ITextEditProvider::GetConversionTarget
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
 - ITextEditProvider.GetConversionTarget
---

# ITextEditProvider::GetConversionTarget


## -description

Returns the current conversion target range.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Pointer to the conversion target range (none if there is no conversion).

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
