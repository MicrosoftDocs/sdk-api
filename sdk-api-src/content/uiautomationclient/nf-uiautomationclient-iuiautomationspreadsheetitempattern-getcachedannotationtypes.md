---
UID: NF:uiautomationclient.IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationTypes
title: IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes
author: windows-sdk-content
description: Retrieves a cached array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell.
old-location: winauto\uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationTypes.htm
old-project: WinAuto
ms.assetid: CF146EB3-AF26-40C0-A19C-78692EE76E92
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCachedAnnotationTypes, GetCachedAnnotationTypes method [Windows Accessibility], GetCachedAnnotationTypes method [Windows Accessibility],IUIAutomationSpreadsheetItemPattern interface, IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility],GetCachedAnnotationTypes method, IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationTypes, IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes, uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes, winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationTypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes


## -description


Retrieves a cached array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell. 


## -parameters




### -param retVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives the cached array of annotation type identifiers. For a list of possible values, see <a href="https://msdn.microsoft.com/46948B7C-EC9F-4B55-B769-62EE8BE11D33">Annotation Type Identifiers</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/4B90ED28-5F85-4F36-8F11-1F2B60CEC9E5">IUIAutomationSpreadsheetItemPattern</a>
 

 

