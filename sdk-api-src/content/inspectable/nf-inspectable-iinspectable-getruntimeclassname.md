---
UID: NF:inspectable.IInspectable.GetRuntimeClassName
title: IInspectable::GetRuntimeClassName (inspectable.h)
description: Gets the fully qualified name of the current Windows Runtime object.
helpviewer_keywords: ["GetRuntimeClassName","GetRuntimeClassName method [Windows Runtime]","GetRuntimeClassName method [Windows Runtime]","IInputPaneInterop interface","GetRuntimeClassName method [Windows Runtime]","IInspectable interface","IInputPaneInterop interface [Windows Runtime]","GetRuntimeClassName method","IInputPaneInterop::GetRuntimeClassName","IInspectable interface [Windows Runtime]","GetRuntimeClassName method","IInspectable.GetRuntimeClassName","IInspectable::GetRuntimeClassName","inspectable/IInputPaneInterop::GetRuntimeClassName","inspectable/IInspectable::GetRuntimeClassName","winrt.iinspectable_getruntimeclassname"]
old-location: winrt\iinspectable_getruntimeclassname.htm
tech.root: WinRT
ms.assetid: E0A0B56D-E676-46FD-873D-11309102DFFD
ms.date: 12/05/2018
ms.keywords: GetRuntimeClassName, GetRuntimeClassName method [Windows Runtime], GetRuntimeClassName method [Windows Runtime],IInputPaneInterop interface, GetRuntimeClassName method [Windows Runtime],IInspectable interface, IInputPaneInterop interface [Windows Runtime],GetRuntimeClassName method, IInputPaneInterop::GetRuntimeClassName, IInspectable interface [Windows Runtime],GetRuntimeClassName method, IInspectable.GetRuntimeClassName, IInspectable::GetRuntimeClassName, inspectable/IInputPaneInterop::GetRuntimeClassName, inspectable/IInspectable::GetRuntimeClassName, winrt.iinspectable_getruntimeclassname
req.header: inspectable.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inspectable.idl
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
 - IInspectable::GetRuntimeClassName
 - inspectable/IInspectable::GetRuntimeClassName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inspectable.h
api_name:
 - IInspectable.GetRuntimeClassName
 - IInputPaneInterop.GetRuntimeClassName
---

## -description

Gets the fully qualified name of the current Windows Runtime object.

## -parameters

### -param className [out]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>*</b>

The fully qualified name of the current Windows Runtime object.

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
The  <i>className</i> string was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate <i>className</i> string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
<i>className</i> refers to a class factory or a static interface.

</td>
</tr>
</table>

## -remarks

Use the <b>GetRuntimeClassName</b> method to retrieve the namespace-qualified name of a Windows Runtime object.

The caller is responsible for freeing the <i>className</i> string by using the <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a> function.   

The following table shows example class name strings that could be returned by the <b>GetRuntimeClassName</b> method.


<table>
<tr>
<th>Example Class Name</th>
<th>Description</th>
</tr>
<tr>
<td>Fabrikam.Kitchen.IToaster</td>
<td>An interface in the Fabrikam.Kitchen namespace. </td>
</tr>
<tr>
<td>Fabrikam.Kitchen.Chef</td>
<td>An class in the Fabrikam.Kitchen namespace. </td>
</tr>
<tr>
<td>Windows.Foundation.Collections.IVector`1&lt;TailspinToys.IStore&gt;</td>
<td>A vector of TailspinToys.IStore interfaces. </td>
</tr>
<tr>
<td>Windows.Foundation.Collections.IVector`1&lt;Windows.Foundation.Collections.IMap`2&lt;String, TailspinToys.IStore&gt;&gt;</td>
<td>A vector of maps of strings to TailspinToys.IStore interfaces. </td>
</tr>
</table>
 



The <b>GetRuntimeClassName</b> method provides the most specific type information that the server object guarantees that it implements. The type name may be a runtime class name, interface group name, interface name, or parameterized interface name. 

The <b>GetRuntimeClassName</b> method returns <b>E_ILLEGAL_METHOD_CALL</b> if the class name refers to a class factory or a static interface.

## -see-also

<a href="/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop">IInputPaneInterop</a>

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>

[winrt::get_class_name](/uwp/cpp-ref-for-winrt/get-class-name)
