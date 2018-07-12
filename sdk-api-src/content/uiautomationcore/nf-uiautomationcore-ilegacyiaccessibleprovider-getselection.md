---
UID: NF:uiautomationcore.ILegacyIAccessibleProvider.GetSelection
title: ILegacyIAccessibleProvider::GetSelection
author: windows-sdk-content
description: Retrieves the selected item or items in the control.
old-location: winauto\uiauto_ILegacyIAccessibleProvider_GetSelection.htm
old-project: WinAuto
ms.assetid: 8436e554-2f09-46ed-a32a-0d2612bc60fb
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetSelection, GetSelection method [Windows Accessibility], GetSelection method [Windows Accessibility],ILegacyIAccessibleProvider interface, ILegacyIAccessibleProvider interface [Windows Accessibility],GetSelection method, ILegacyIAccessibleProvider.GetSelection, ILegacyIAccessibleProvider::GetSelection, uiauto.uiauto_ILegacyIAccessibleProvider_GetSelection, uiauto_ILegacyIAccessibleProvider_GetSelection, uiautomationcore/ILegacyIAccessibleProvider::GetSelection, winauto.uiauto_ILegacyIAccessibleProvider_GetSelection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
 - Uiautomationcore.dll
api_name:
 - ILegacyIAccessibleProvider.GetSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILegacyIAccessibleProvider::GetSelection


## -description


Retrieves the selected item or items in the control.


## -parameters




### -param pvarSelectedChildren [out]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> containing the selected items.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9d911238-05d9-4bba-920f-40ca23ab9549">ILegacyIAccessibleProvider</a>



<b>Reference</b>
 

 

