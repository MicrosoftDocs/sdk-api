---
UID: NF:uiautomationcore.IRawElementProviderFragmentRoot.GetFocus
title: IRawElementProviderFragmentRoot::GetFocus
author: windows-sdk-content
description: Retrieves the element in this fragment that has the input focus.
old-location: winauto\uiauto_IRawElementProviderFragmentRoot_GetFocus.htm
tech.root: WinAuto
ms.assetid: 73b5ffc8-1a24-4fa5-8bc4-ae09656a80df
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetFocus, GetFocus method [Windows Accessibility], GetFocus method [Windows Accessibility],IRawElementProviderFragmentRoot interface, IRawElementProviderFragmentRoot interface [Windows Accessibility],GetFocus method, IRawElementProviderFragmentRoot.GetFocus, IRawElementProviderFragmentRoot::GetFocus, uiauto.uiauto_IRawElementProviderFragmentRoot_GetFocus, uiauto_IRawElementProviderFragmentRoot_GetFocus, uiautomationcore/IRawElementProviderFragmentRoot::GetFocus, winauto.uiauto_IRawElementProviderFragmentRoot_GetFocus
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
 - IRawElementProviderFragmentRoot.GetFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderFragmentRoot::GetFocus


## -description


Retrieves the element in this fragment that has the input focus.


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>**</b>

Receives a pointer to the <a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a> 
                interface of the
				element in this fragment that has the input focus, if any; otherwise <b>NULL</b>. 
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a>
 

 

