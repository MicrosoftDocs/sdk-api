---
UID: NF:uiautomationclient.IUIAutomation.CompareRuntimeIds
title: IUIAutomation::CompareRuntimeIds
author: windows-sdk-content
description: Compares two integer arrays containing run-time identifiers (IDs) to determine whether their content is the same and they belong to the same UI element.
old-location: winauto\uiauto_IUIAutomation_CompareRuntimeIds.htm
tech.root: WinAuto
ms.assetid: b0c481eb-3545-439c-bf6a-347b98ea35de
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: CompareRuntimeIds, CompareRuntimeIds method [Windows Accessibility], CompareRuntimeIds method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CompareRuntimeIds method, IUIAutomation.CompareRuntimeIds, IUIAutomation::CompareRuntimeIds, uiauto.uiauto_IUIAutomation_CompareRuntimeIds, uiauto_IUIAutomation_CompareRuntimeIds, uiautomationclient/IUIAutomation::CompareRuntimeIds, winauto.uiauto_IUIAutomation_CompareRuntimeIds
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
 - IUIAutomation.CompareRuntimeIds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::CompareRuntimeIds


## -description


Compares two integer arrays containing run-time identifiers (IDs) to determine whether their content is the same and they belong to the same UI element.


## -parameters




### -param runtimeId1 [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

The first ID to compare.


### -param runtimeId2 [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

The second ID to compare


### -param areSame [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Receives <b>TRUE</b> if the IDs are the same, or <b>FALSE</b> otherwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/e4daa3c3-24fb-41df-a1b1-bd6545a47e51">CompareElements</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d351f2ca-d9de-4055-8356-9a100a77f397">GetRuntimeId</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<b>Reference</b>
 

 

