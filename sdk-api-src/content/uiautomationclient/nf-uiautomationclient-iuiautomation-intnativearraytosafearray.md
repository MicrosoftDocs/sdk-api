---
UID: NF:uiautomationclient.IUIAutomation.IntNativeArrayToSafeArray
title: IUIAutomation::IntNativeArrayToSafeArray (uiautomationclient.h)
description: Converts an array of integers to a SAFEARRAY.
helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","IntNativeArrayToSafeArray method","IUIAutomation.IntNativeArrayToSafeArray","IUIAutomation::IntNativeArrayToSafeArray","IntNativeArrayToSafeArray","IntNativeArrayToSafeArray method [Windows Accessibility]","IntNativeArrayToSafeArray method [Windows Accessibility]","IUIAutomation interface","uiauto.uiauto_IUIAutomation_IntNativeArrayToSafeArray","uiauto_IUIAutomation_IntNativeArrayToSafeArray","uiautomationclient/IUIAutomation::IntNativeArrayToSafeArray","winauto.uiauto_IUIAutomation_IntNativeArrayToSafeArray"]
old-location: winauto\uiauto_IUIAutomation_IntNativeArrayToSafeArray.htm
tech.root: WinAuto
ms.assetid: f8fd2c2b-f8c7-454b-ad03-aeeb4bbcef61
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],IntNativeArrayToSafeArray method, IUIAutomation.IntNativeArrayToSafeArray, IUIAutomation::IntNativeArrayToSafeArray, IntNativeArrayToSafeArray, IntNativeArrayToSafeArray method [Windows Accessibility], IntNativeArrayToSafeArray method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_IntNativeArrayToSafeArray, uiauto_IUIAutomation_IntNativeArrayToSafeArray, uiautomationclient/IUIAutomation::IntNativeArrayToSafeArray, winauto.uiauto_IUIAutomation_IntNativeArrayToSafeArray
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation::IntNativeArrayToSafeArray
 - uiautomationclient/IUIAutomation::IntNativeArrayToSafeArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.IntNativeArrayToSafeArray
---

# IUIAutomation::IntNativeArrayToSafeArray


## -description

Converts an array of integers to a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>.

## -parameters

### -param array [in]

Type: <b>int*</b>

A pointer to an array of integers.

### -param arrayCount [in]

Type: <b>int</b>

The number of elements in <i>array</i>.

### -param safeArray [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to the allocated SAFEARRAY.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray">IUIAutomation::IntSafeArrayToNativeArray</a>