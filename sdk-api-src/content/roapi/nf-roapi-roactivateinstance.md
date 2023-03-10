---
UID: NF:roapi.RoActivateInstance
title: RoActivateInstance function (roapi.h)
description: Activates the specified Windows Runtime class.
helpviewer_keywords: ["RoActivateInstance","RoActivateInstance function [Windows Runtime]","WinRTActivateInstance","roapi/RoActivateInstance","roapi/WinRTActivateInstance","winrt.roactivateinstance","winrt.winrtactivateinstance"]
old-location: winrt\roactivateinstance.htm
tech.root: WinRT
ms.assetid: 20E469FE-100B-489F-956A-347716FA8A12
ms.date: 12/05/2018
ms.keywords: RoActivateInstance, RoActivateInstance function [Windows Runtime], WinRTActivateInstance, roapi/RoActivateInstance, roapi/WinRTActivateInstance, winrt.roactivateinstance, winrt.winrtactivateinstance
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoActivateInstance
 - roapi/RoActivateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - roapi.h
 - API-MS-Win-Core-WinRT-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoActivateInstance
 - WinRTActivateInstance
---

# RoActivateInstance function


## -description

Activates the specified Windows Runtime class.

## -parameters

### -param activatableClassId [in]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

The class identifier that is associated with the activatable runtime class.

### -param instance [out]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to the activated instance of the runtime class.

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
The class was activated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>instance</i> is <b>NULL</b>.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/inspectable/ne-inspectable-trustlevel">TrustLevel</a> for the class requires a full-trust process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface is not implemented by the specified class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to create an instance of the class.

</td>
</tr>
</table>

## -remarks

Use the <b>RoActivateInstance</b> function to activate a Windows Runtime class. The <b>RoActivateInstance</b> function connects to the activation factory that is associated with the specified activatable class identifier, creates an instance by calling the zero-argument constructor on the class, and releases the activation factory.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/activation/nn-activation-iactivationfactory">IActivationFactory</a>



<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>



<a href="/windows/desktop/api/inspectable/ne-inspectable-trustlevel">TrustLevel</a>