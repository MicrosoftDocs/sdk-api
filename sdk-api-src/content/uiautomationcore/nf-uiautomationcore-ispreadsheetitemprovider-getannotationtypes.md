---
UID: NF:uiautomationcore.ISpreadsheetItemProvider.GetAnnotationTypes
title: ISpreadsheetItemProvider::GetAnnotationTypes
author: windows-sdk-content
description: Retrieves an array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell.
old-location: winauto\uiauto_ISpreadsheetItemProvider_GetAnnotationTypes.htm
tech.root: WinAuto
ms.assetid: 95DD80C7-AD98-42D5-BB2E-05ACA02F878A
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetAnnotationTypes, GetAnnotationTypes method [Windows Accessibility], GetAnnotationTypes method [Windows Accessibility],ISpreadsheetItemProvider interface, ISpreadsheetItemProvider interface [Windows Accessibility],GetAnnotationTypes method, ISpreadsheetItemProvider.GetAnnotationTypes, ISpreadsheetItemProvider::GetAnnotationTypes, uiautomationcore/ISpreadsheetItemProvider::GetAnnotationTypes, winauto.uiauto_ISpreadsheetItemProvider_GetAnnotationTypes
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
 - ISpreadsheetItemProvider.GetAnnotationTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpreadsheetItemProvider::GetAnnotationTypes


## -description


Retrieves an array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell. 


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives an array of annotation type identifiers, one for each type of annotation associated with the spreadsheet cell. For a list of possible values, see <a href="https://msdn.microsoft.com/46948B7C-EC9F-4B55-B769-62EE8BE11D33">Annotation Type Identifiers</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/E6428FED-2BCC-4AD5-B612-A22899624538">ISpreadsheetItemProvider</a>
 

 

