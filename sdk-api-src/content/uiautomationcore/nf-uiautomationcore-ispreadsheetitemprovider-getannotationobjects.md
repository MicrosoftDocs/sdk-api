---
UID: NF:uiautomationcore.ISpreadsheetItemProvider.GetAnnotationObjects
title: ISpreadsheetItemProvider::GetAnnotationObjects
author: windows-sdk-content
description: Retrieves an array of objects that represent the annotations associated with this spreadsheet cell.
old-location: winauto\uiauto_ISpreadsheetItemProvider_GetAnnotationObjects.htm
tech.root: WinAuto
ms.assetid: 5B9BDAF8-A7A7-492B-97F7-8502E630203F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAnnotationObjects, GetAnnotationObjects method [Windows Accessibility], GetAnnotationObjects method [Windows Accessibility],ISpreadsheetItemProvider interface, ISpreadsheetItemProvider interface [Windows Accessibility],GetAnnotationObjects method, ISpreadsheetItemProvider.GetAnnotationObjects, ISpreadsheetItemProvider::GetAnnotationObjects, uiautomationcore/ISpreadsheetItemProvider::GetAnnotationObjects, winauto.uiauto_ISpreadsheetItemProvider_GetAnnotationObjects
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
 - ISpreadsheetItemProvider.GetAnnotationObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpreadsheetItemProvider::GetAnnotationObjects


## -description


Retrieves an array of objects that represent the annotations associated with this spreadsheet cell.


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives an array of <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interfaces that represent the annotations associated with the spreadsheet cell.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/E6428FED-2BCC-4AD5-B612-A22899624538">ISpreadsheetItemProvider</a>
 

 

