---
UID: NF:uiautomationcore.ITextRangeProvider.Clone
title: ITextRangeProvider::Clone
author: windows-sdk-content
description: Returns a new ITextRangeProvider identical to the original ITextRangeProvider and inheriting all properties of the original.
old-location: winauto\uiauto_ITextRangeProvider_Clone.htm
tech.root: WinAuto
ms.assetid: fe55f57b-a803-4008-adfb-b1900550d4cb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Clone, Clone method [Windows Accessibility], Clone method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],Clone method, ITextRangeProvider.Clone, ITextRangeProvider::Clone, uiauto.uiauto_ITextRangeProvider_Clone, uiauto_ITextRangeProvider_Clone, uiautomationcore/ITextRangeProvider::Clone, winauto.uiauto_ITextRangeProvider_Clone
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
 - ITextRangeProvider.Clone
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
- ITextRangeProvider.Clone
: 
---

# ITextRangeProvider::Clone


## -description


Returns a new <a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a> identical to the original 
        <b>ITextRangeProvider</b> and inheriting all properties of the original.
        


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>**</b>

Receives a pointer to 
                the copy of the text range. 
                A null reference is never returned.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The new range can be manipulated independently from the original.





## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

