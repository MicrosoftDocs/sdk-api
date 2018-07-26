---
UID: NF:uiautomationcore.ITextRangeProvider.GetAttributeValue
title: ITextRangeProvider::GetAttributeValue
author: windows-sdk-content
description: Retrieves the value of the specified text attribute across the text range.
old-location: winauto\uiauto_ITextRangeProvider_GetAttributeValue.htm
old-project: WinAuto
ms.assetid: a72e780e-30e3-4feb-8f47-46b9f1714061
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetAttributeValue, GetAttributeValue method [Windows Accessibility], GetAttributeValue method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetAttributeValue method, ITextRangeProvider.GetAttributeValue, ITextRangeProvider::GetAttributeValue, uiauto.uiauto_ITextRangeProvider_GetAttributeValue, uiauto_ITextRangeProvider_GetAttributeValue, uiautomationcore/ITextRangeProvider::GetAttributeValue, winauto.uiauto_ITextRangeProvider_GetAttributeValue
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider.GetAttributeValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRangeProvider::GetAttributeValue


## -description


Retrieves the value of the specified text attribute across the text range.  


## -parameters




### -param attributeId [in]

Type: <b>TEXTATTRIBUTEID</b>

The identifier of the text attribute. For a list of text attribute IDs, see <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>*</b>

Receives one of the following. 

<ul>
<li>The address of an object representing the value of the specified attribute. The data type of the value varies depending on the specified attribute. For example, if <i>attributeId</i> is <a href="https://msdn.microsoft.com/library/Ee671662(v=VS.85).aspx">UIA_FontNameAttributeId</a>,  <b>GetAttributeValue</b> returns a string that represents the font name of the text range,  but if <i>attributeId</i> is <a href="https://msdn.microsoft.com/library/Ee671662(v=VS.85).aspx">UIA_IsItalicAttributeId</a>,  <b>GetAttributeValue</b> returns a boolean.



</li>
<li>The address of the value retrieved by the <a href="https://msdn.microsoft.com/597ace91-197a-4cda-9386-78c6e429871b">UiaGetReservedMixedAttributeValue</a> function, if the value of the specified attribute varies over the text range.</li>
<li>The address of the value retrieved by the <a href="https://msdn.microsoft.com/ba789ed0-fa34-492c-90b4-acee0adb634c">UiaGetReservedNotSupportedValue</a> function, if the specified attribute is not supported by the provider or the control. </li>
</ul>

				This parameter is passed uninitialized. 
                


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>GetAttributeValue</b> method should retrieve the attribute value regardless of whether the text is hidden or visible.
            




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

