---
UID: NF:uiautomationclient.IUIAutomation.IntSafeArrayToNativeArray
title: IUIAutomation::IntSafeArrayToNativeArray (uiautomationclient.h)
description: Converts a SAFEARRAY of integers to an array.
helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","IntSafeArrayToNativeArray method","IUIAutomation.IntSafeArrayToNativeArray","IUIAutomation::IntSafeArrayToNativeArray","IntSafeArrayToNativeArray","IntSafeArrayToNativeArray method [Windows Accessibility]","IntSafeArrayToNativeArray method [Windows Accessibility]","IUIAutomation interface","uiauto.uiauto_IUIAutomation_IntSafeArrayToNativeArray","uiauto_IUIAutomation_IntSafeArrayToNativeArray","uiautomationclient/IUIAutomation::IntSafeArrayToNativeArray","winauto.uiauto_IUIAutomation_IntSafeArrayToNativeArray"]
old-location: winauto\uiauto_IUIAutomation_IntSafeArrayToNativeArray.htm
tech.root: WinAuto
ms.assetid: 422b1bfc-5f67-4ba5-b573-d3dce9b6d806
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],IntSafeArrayToNativeArray method, IUIAutomation.IntSafeArrayToNativeArray, IUIAutomation::IntSafeArrayToNativeArray, IntSafeArrayToNativeArray, IntSafeArrayToNativeArray method [Windows Accessibility], IntSafeArrayToNativeArray method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_IntSafeArrayToNativeArray, uiauto_IUIAutomation_IntSafeArrayToNativeArray, uiautomationclient/IUIAutomation::IntSafeArrayToNativeArray, winauto.uiauto_IUIAutomation_IntSafeArrayToNativeArray
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
 - IUIAutomation::IntSafeArrayToNativeArray
 - uiautomationclient/IUIAutomation::IntSafeArrayToNativeArray
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
 - IUIAutomation.IntSafeArrayToNativeArray
---

# IUIAutomation::IntSafeArrayToNativeArray


## -description

Converts a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> of integers to an array.

## -parameters

### -param intArray [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A pointer to the SAFEARRAY to convert.

### -param array [out]

Type: <b>int**</b>

Receives a pointer to the allocated array.

### -param arrayCount [out, retval]

Type: <b>int*</b>

Receives the number of elements in <i>array</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray">IntNativeArrayToSafeArray</a>