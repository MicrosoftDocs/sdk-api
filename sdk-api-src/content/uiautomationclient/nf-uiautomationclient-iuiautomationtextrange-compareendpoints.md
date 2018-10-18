---
UID: NF:uiautomationclient.IUIAutomationTextRange.CompareEndpoints
title: IUIAutomationTextRange::CompareEndpoints
author: windows-sdk-content
description: Retrieves a value that specifies whether the start or end endpoint of this text range is the same as the start or end endpoint of another text range.
old-location: winauto\uiauto_IUIAutomationTextRange_CompareEndpoints.htm
tech.root: WinAuto
ms.assetid: 7071ae46-3f2d-4fdb-9908-366ac1fde691
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CompareEndpoints, CompareEndpoints method [Windows Accessibility], CompareEndpoints method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],CompareEndpoints method, IUIAutomationTextRange.CompareEndpoints, IUIAutomationTextRange::CompareEndpoints, uiauto.uiauto_IUIAutomationTextRange_CompareEndpoints, uiauto_IUIAutomationTextRange_CompareEndpoints, uiautomationclient/IUIAutomationTextRange::CompareEndpoints, winauto.uiauto_IUIAutomationTextRange_CompareEndpoints
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
 - IUIAutomationTextRange.CompareEndpoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange::CompareEndpoints


## -description


Retrieves a value that specifies whether the start or end endpoint of this text range is the same as the start or end endpoint of another text range.


## -parameters




### -param arg1

TBD


### -param range [in]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>*</b>

A pointer to the text range to compare.


### -param arg2

TBD


### -param compValue [out, retval]

Type: <b>int*</b>

Receives a negative value if the caller's endpoint occurs earlier in the text than the target endpoint; 0 if the caller's endpoint is at the same location as the target endpoint; or a positive value if the caller's endpoint occurs later in the text than the target endpoint.


#### - srcEndPoint [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

A value indicating whether the start or end endpoint of this text range is to be compared.


#### - targetEndPoint [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

A value indicating whether the start or end endpoint of <i>range</i> is to be compared.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

