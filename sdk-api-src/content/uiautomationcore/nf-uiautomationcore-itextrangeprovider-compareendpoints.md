---
UID: NF:uiautomationcore.ITextRangeProvider.CompareEndpoints
title: ITextRangeProvider::CompareEndpoints
author: windows-sdk-content
description: Returns a value that specifies whether two text ranges have identical endpoints.
old-location: winauto\uiauto_ITextRangeProvider_CompareEndpoints.htm
tech.root: WinAuto
ms.assetid: 88a59d93-f31b-40d5-a8d9-ef114224019b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CompareEndpoints, CompareEndpoints method [Windows Accessibility], CompareEndpoints method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],CompareEndpoints method, ITextRangeProvider.CompareEndpoints, ITextRangeProvider::CompareEndpoints, uiauto.uiauto_ITextRangeProvider_CompareEndpoints, uiauto_ITextRangeProvider_CompareEndpoints, uiautomationcore/ITextRangeProvider::CompareEndpoints, winauto.uiauto_ITextRangeProvider_CompareEndpoints
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
 - ITextRangeProvider.CompareEndpoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRangeProvider::CompareEndpoints


## -description


Returns a value that specifies whether two text ranges have identical endpoints.    
        


## -parameters




### -param arg1 [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

The endpoint (starting or ending) of the caller's text range.


### -param targetRange [in]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>*</b>

The text range to be compared.


### -param arg2

TBD


### -param pRetVal [out, retval]

Type: <b>int*</b>

Receives a value that indicates whether the two text ranges have identical endpoints.
				 This parameter is passed uninitialized.


#### - arg3 [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

The endpoint (starting or ending) of the target text range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Returns a negative value if the caller's endpoint occurs earlier in the text than the target endpoint. 


Returns zero if the caller's endpoint is at the same location as the target endpoint. 


Returns a positive value if the caller's endpoint occurs later in the text than the target endpoint. 
			




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

