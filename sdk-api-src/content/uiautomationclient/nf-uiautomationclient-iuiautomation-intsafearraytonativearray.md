---
UID: NF:uiautomationclient.IUIAutomation.IntSafeArrayToNativeArray
title: IUIAutomation::IntSafeArrayToNativeArray
author: windows-sdk-content
description: Converts a SAFEARRAY of integers to an array.
old-location: winauto\uiauto_IUIAutomation_IntSafeArrayToNativeArray.htm
tech.root: WinAuto
ms.assetid: 422b1bfc-5f67-4ba5-b573-d3dce9b6d806
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],IntSafeArrayToNativeArray method, IUIAutomation.IntSafeArrayToNativeArray, IUIAutomation::IntSafeArrayToNativeArray, IntSafeArrayToNativeArray, IntSafeArrayToNativeArray method [Windows Accessibility], IntSafeArrayToNativeArray method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_IntSafeArrayToNativeArray, uiauto_IUIAutomation_IntSafeArrayToNativeArray, uiautomationclient/IUIAutomation::IntSafeArrayToNativeArray, winauto.uiauto_IUIAutomation_IntSafeArrayToNativeArray
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
 - IUIAutomation.IntSafeArrayToNativeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::IntSafeArrayToNativeArray


## -description


Converts a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> of integers to an array.


## -parameters




### -param intArray [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the SAFEARRAY to convert.


### -param array [out]

Type: <b>int**</b>

Receives a pointer to the allocated array.


### -param arrayCount [out, retval]

Type: <b>int*</b>

Receives the number of elements in <i>array</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/f8fd2c2b-f8c7-454b-ad03-aeeb4bbcef61">IntNativeArrayToSafeArray</a>
 

 

