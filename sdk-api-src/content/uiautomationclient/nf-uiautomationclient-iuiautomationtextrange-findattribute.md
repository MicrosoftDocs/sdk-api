---
UID: NF:uiautomationclient.IUIAutomationTextRange.FindAttribute
title: IUIAutomationTextRange::FindAttribute
author: windows-sdk-content
description: Retrieves a text range subset that has the specified text attribute value.
old-location: winauto\uiauto_IUIAutomationTextRange_FindAttribute.htm
tech.root: WinAuto
ms.assetid: 12722d22-79ca-4390-8155-61234b821256
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: FindAttribute, FindAttribute method [Windows Accessibility], FindAttribute method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],FindAttribute method, IUIAutomationTextRange.FindAttribute, IUIAutomationTextRange::FindAttribute, uiauto.uiauto_IUIAutomationTextRange_FindAttribute, uiauto_IUIAutomationTextRange_FindAttribute, uiautomationclient/IUIAutomationTextRange::FindAttribute, winauto.uiauto_IUIAutomationTextRange_FindAttribute
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
 - IUIAutomationTextRange.FindAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange::FindAttribute


## -description


Retrieves a text range subset that has the specified text attribute value.


## -parameters




### -param attr [in]

Type: <b>TEXTATTRIBUTEID</b>

The identifier of the text attribute for the text range subset being retrieved. For a list of text attribute IDs, see <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>.


### -param val [in]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a></b>

The value of the attribute. This value must match the type specified for the attribute.


### -param backward [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>.


### -param found [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a pointer to the text range having a matching attribute and attribute value; otherwise <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>FindAttribute</b> method retrieves matching text regardless of whether the text is hidden or visible. Use <a href="uiauto_textattribute_ids.htm">UIA_IsHiddenAttributeId</a> to check text visibility.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

