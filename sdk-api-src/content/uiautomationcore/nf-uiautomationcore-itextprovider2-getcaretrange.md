---
UID: NF:uiautomationcore.ITextProvider2.GetCaretRange
title: ITextProvider2::GetCaretRange
author: windows-sdk-content
description: Provides a zero-length text range at the location of the caret that belongs to the text-based control.
old-location: winauto\uiauto_ITextProvider2_GetCaretRange.htm
tech.root: WinAuto
ms.assetid: 9DD77361-25E8-40A3-BDF4-AFE06F9D36F4
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetCaretRange, GetCaretRange method [Windows Accessibility], GetCaretRange method [Windows Accessibility],ITextProvider2 interface, ITextProvider2 interface [Windows Accessibility],GetCaretRange method, ITextProvider2.GetCaretRange, ITextProvider2::GetCaretRange, uiautomationcore/ITextProvider2::GetCaretRange, winauto.uiauto_ITextProvider2_GetCaretRange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ITextProvider2.GetCaretRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextProvider2::GetCaretRange


## -description


Provides a zero-length text range at the location of the caret that belongs to the text-based control.


## -parameters




### -param isActive [out]

Type: <b>BOOL*</b>

<b>TRUE</b> if the text-based control that contains the caret has keyboard focus, otherwise <b>FALSE</b>.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>**</b>

 A text range that represents the current location of the caret that belongs to the text-based control. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>isActive</i> parameter is <b>FALSE</b>, the caret that belongs to the text-based control might not be at the same location as the system caret.

This method retrieves a text range that a client can use to find the bounding rectangle of the caret that belongs to the text-based control, or to find the text near the caret.




## -see-also




<a href="https://msdn.microsoft.com/CDA6E93D-6E82-4EC4-8408-09554D039F49">ITextProvider2</a>
 

 

