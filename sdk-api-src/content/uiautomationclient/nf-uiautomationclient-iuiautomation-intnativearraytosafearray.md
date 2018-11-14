---
UID: NF:uiautomationclient.IUIAutomation.IntNativeArrayToSafeArray
title: IUIAutomation::IntNativeArrayToSafeArray
author: windows-sdk-content
description: Converts an array of integers to a SAFEARRAY.
old-location: winauto\uiauto_IUIAutomation_IntNativeArrayToSafeArray.htm
tech.root: WinAuto
ms.assetid: f8fd2c2b-f8c7-454b-ad03-aeeb4bbcef61
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],IntNativeArrayToSafeArray method, IUIAutomation.IntNativeArrayToSafeArray, IUIAutomation::IntNativeArrayToSafeArray, IntNativeArrayToSafeArray, IntNativeArrayToSafeArray method [Windows Accessibility], IntNativeArrayToSafeArray method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_IntNativeArrayToSafeArray, uiauto_IUIAutomation_IntNativeArrayToSafeArray, uiautomationclient/IUIAutomation::IntNativeArrayToSafeArray, winauto.uiauto_IUIAutomation_IntNativeArrayToSafeArray
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
 - IUIAutomation.IntNativeArrayToSafeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomation.IntNativeArrayToSafeArray
: 
---

# IUIAutomation::IntNativeArrayToSafeArray


## -description


Converts an array of integers to a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>.


## -parameters




### -param array [in]

Type: <b>int*</b>

A pointer to an array of integers.


### -param arrayCount [in]

Type: <b>int</b>

The number of elements in <i>array</i>.


### -param safeArray [out, retval]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to the allocated SAFEARRAY.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/422b1bfc-5f67-4ba5-b573-d3dce9b6d806">IUIAutomation::IntSafeArrayToNativeArray</a>
 

 

