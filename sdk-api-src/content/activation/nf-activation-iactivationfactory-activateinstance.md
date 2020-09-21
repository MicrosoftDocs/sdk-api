---
UID: NF:activation.IActivationFactory.ActivateInstance
title: IActivationFactory::ActivateInstance (activation.h)
description: Creates a new instance of the Windows Runtime class that is associated with the current activation factory.
helpviewer_keywords: ["ActivateInstance","ActivateInstance method [Windows Runtime]","ActivateInstance method [Windows Runtime]","IActivationFactory interface","IActivationFactory interface [Windows Runtime]","ActivateInstance method","IActivationFactory.ActivateInstance","IActivationFactory::ActivateInstance","activation/IActivationFactory::ActivateInstance","winrt.iactivationfactory_activateinstance"]
old-location: winrt\iactivationfactory_activateinstance.htm
tech.root: WinRT
ms.assetid: AE3E2D87-3AE7-42C3-AA1D-510E717D2E51
ms.date: 12/05/2018
ms.keywords: ActivateInstance, ActivateInstance method [Windows Runtime], ActivateInstance method [Windows Runtime],IActivationFactory interface, IActivationFactory interface [Windows Runtime],ActivateInstance method, IActivationFactory.ActivateInstance, IActivationFactory::ActivateInstance, activation/IActivationFactory::ActivateInstance, winrt.iactivationfactory_activateinstance
req.header: activation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Activation.idl
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
 - IActivationFactory::ActivateInstance
 - activation/IActivationFactory::ActivateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activation.h
api_name:
 - IActivationFactory.ActivateInstance
---

# IActivationFactory::ActivateInstance


## -description

Creates a new instance of the Windows Runtime class that is associated with the current activation factory.

## -parameters

### -param instance [out]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new instance of the class that is associated with the current activation factory.

## -returns

Type: <b>HRESULT</b>

This function can return the following values.

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
The  new class instance was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>instance</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface is not implemented by the class that is associated with the current activation factory.

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

Use the <b>ActivateInstance</b> function to activate a Windows Runtime class. The <b>ActivateInstance</b> function connects to the activation factory that is associated with the specified activatable class identifier, creates an instance by calling the zero-argument constructor on the class, and releases the activation factory.

## -see-also

<a href="/windows/desktop/api/activation/nn-activation-iactivationfactory">IActivationFactory</a>



<a href="/windows/desktop/api/roapi/nf-roapi-roactivateinstance">RoActivateInstance</a>