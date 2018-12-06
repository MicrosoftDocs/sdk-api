---
UID: NF:uiautomationcore.ITextEditProvider.GetConversionTarget
title: ITextEditProvider::GetConversionTarget
author: windows-sdk-content
description: Returns the current conversion target range.
old-location: winauto\uiauto_ITextEditProvider_GetConversionTarget.htm
tech.root: WinAuto
ms.assetid: C05DC0F6-FB24-2D06-C2D8-43ADF2C110F9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetConversionTarget, GetConversionTarget method [Windows Accessibility], GetConversionTarget method [Windows Accessibility],ITextEditProvider interface, ITextEditProvider interface [Windows Accessibility],GetConversionTarget method, ITextEditProvider.GetConversionTarget, ITextEditProvider::GetConversionTarget, uiautomationcore/ITextEditProvider::GetConversionTarget, winauto.uiauto_ITextEditProvider_GetConversionTarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextEditProvider.GetConversionTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextEditProvider::GetConversionTarget


## -description


Returns the current conversion target range.


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>**</b>

Pointer to the conversion target range (none if there is no conversion).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Follow the guidance given in <a href="https://msdn.microsoft.com/AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9">TextEdit Control Pattern</a> that describes how to implement this method and how to raise the related notification events.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6AA3F2A5-B34C-F7CB-13B3-6C62E2B67326">ITextEditProvider</a>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9">TextEdit Control Pattern</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>



<a href="https://msdn.microsoft.com/19E7C2C1-D0D5-672F-FC6F-8E1B8CC19819">UiaRaiseTextEditTextChangedEvent</a>
 

 

