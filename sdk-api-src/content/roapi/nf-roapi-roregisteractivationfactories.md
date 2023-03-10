---
UID: NF:roapi.RoRegisterActivationFactories
title: RoRegisterActivationFactories function (roapi.h)
description: Registers an array out-of-process activation factories for a Windows Runtime exe server.
helpviewer_keywords: ["RoRegisterActivationFactories","RoRegisterActivationFactories function [Windows Runtime]","WinRTRegisterActivationFactories","roapi/RoRegisterActivationFactories","roapi/WinRTRegisterActivationFactories","winrt.roregisteractivationfactories","winrt.winrtregisteractivationfactories"]
old-location: winrt\roregisteractivationfactories.htm
tech.root: WinRT
ms.assetid: 8213f5de-3b1c-44c3-ad37-b2ebac8dbcd8
ms.date: 12/05/2018
ms.keywords: RoRegisterActivationFactories, RoRegisterActivationFactories function [Windows Runtime], WinRTRegisterActivationFactories, roapi/RoRegisterActivationFactories, roapi/WinRTRegisterActivationFactories, winrt.roregisteractivationfactories, winrt.winrtregisteractivationfactories
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoRegisterActivationFactories
 - roapi/RoRegisterActivationFactories
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-l1-1-0.dll
api_name:
 - RoRegisterActivationFactories
 - WinRTRegisterActivationFactories
---

# RoRegisterActivationFactories function


## -description

Registers an array out-of-process activation factories for a Windows Runtime exe server.

## -parameters

### -param activatableClassIds [in]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>*</b>

An array of class identifiers that are associated with activatable runtime classes.

### -param activationFactoryCallbacks [in]

Type: <b><a href="/previous-versions/br205771(v=vs.85)">PFNGETACTIVATIONFACTORY</a>*</b>

An array of callback functions that you can use to retrieve the activation factories that correspond with  <i>activatableClassIds</i>.

### -param count [in]

Type: <b>UINT32</b>

The number of items in the <i>activatableClassIds</i> and <i>activationFactoryCallbacks</i> arrays.

### -param cookie [out]

Type: <b><a href="/windows/desktop/WinRT/ro-registration-cookie">RO_REGISTRATION_COOKIE</a>*</b>

A cookie that identifies the registered factories.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The  activation factory was registered successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>cookie</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The thread is in a neutral apartment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The thread has not been initialized in the Windows Runtime by calling the <a href="/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ALREADYINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The factory has been initialized already. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The class is not registered as OutOfProc.

</td>
</tr>
</table>

## -remarks

The <b>RoRegisterActivationFactories</b> function enables an exe server to register multiple activation factories without experiencing a race condition.

## -see-also

<a href="/windows/desktop/WinRT/ro-registration-cookie">RO_REGISTRATION_COOKIE</a>



<a href="/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a>