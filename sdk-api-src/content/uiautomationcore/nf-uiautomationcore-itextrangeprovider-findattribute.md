---
UID: NF:uiautomationcore.ITextRangeProvider.FindAttribute
title: ITextRangeProvider::FindAttribute
author: windows-sdk-content
description: Returns a text range subset that has the specified text attribute value.
old-location: winauto\uiauto_ITextRangeProvider_FindAttribute.htm
tech.root: WinAuto
ms.assetid: 623a9b66-7d8c-44d7-b0c1-5ed8a8b8f0c6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FindAttribute, FindAttribute method [Windows Accessibility], FindAttribute method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],FindAttribute method, ITextRangeProvider.FindAttribute, ITextRangeProvider::FindAttribute, uiauto.uiauto_ITextRangeProvider_FindAttribute, uiauto_ITextRangeProvider_FindAttribute, uiautomationcore/ITextRangeProvider::FindAttribute, winauto.uiauto_ITextRangeProvider_FindAttribute
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
 - ITextRangeProvider.FindAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationcore.h
: 
- ITextRangeProvider.FindAttribute
: 
---

# ITextRangeProvider::FindAttribute


## -description


Returns a text range subset that has the specified text attribute value. 
        


## -parameters




### -param attributeId [in]

Type: <b>TEXTATTRIBUTEID</b>

The identifier of the text attribute. For a list of text attribute IDs, see <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>.


### -param val [in]

Type: <b><a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a></b>

The attribute value to search for. This value must match the type specified for the attribute.


### -param backward [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>. 


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>**</b>

Receives a pointer to the text range having a matching attribute and attribute value; otherwise <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>FindAttribute</b> method retrieves matching text regardless of whether the text is hidden or visible. Clients can use <a href="uiauto_textattribute_ids.htm">UIA_IsHiddenAttributeId</a> to check text visibility.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

