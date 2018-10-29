---
UID: NF:uiautomationcore.ITextRangeProvider.GetText
title: ITextRangeProvider::GetText
author: windows-sdk-content
description: Retrieves the plain text of the range.
old-location: winauto\uiauto_ITextRangeProvider_GetText.htm
tech.root: WinAuto
ms.assetid: f3c5f0cc-15a5-4a13-b3be-355de6633c66
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetText, GetText method [Windows Accessibility], GetText method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetText method, ITextRangeProvider.GetText, ITextRangeProvider::GetText, uiauto.uiauto_ITextRangeProvider_GetText, uiauto_ITextRangeProvider_GetText, uiautomationcore/ITextRangeProvider::GetText, winauto.uiauto_ITextRangeProvider_GetText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - ITextRangeProvider.GetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRangeProvider::GetText


## -description


Retrieves the plain text of the range.


## -parameters




### -param maxLength [in]

Type: <b>int</b>

The maximum length of the string to return. Use -1 if no limit is required.


### -param pRetVal [out, retval]

Type: <b>BSTR*</b>

Receives the plain text of the text range, 
				possibly truncated at the specified maximum length. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>ITextRangeProvider::GetText</b> retrieves both hidden and visible text.

If <i>maxLength</i> is greater 
            than the length of the text span of the caller, the string returned will be the 
			plain text of the text range.

<b>ITextRangeProvider::GetText</b> will not be affected by the order of endpoints in the text flow; 
			it will always return the text between the start and end endpoints of the text range in the logical text flow order.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

