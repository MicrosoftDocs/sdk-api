---
UID: NF:inspectable.IInspectable.GetRuntimeClassName
title: IInspectable::GetRuntimeClassName
author: windows-sdk-content
description: Gets the fully qualified name of the current Windows Runtime object.
old-location: winrt\iinspectable_getruntimeclassname.htm
tech.root: WinRT
ms.assetid: E0A0B56D-E676-46FD-873D-11309102DFFD
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetRuntimeClassName, GetRuntimeClassName method [Windows Runtime], GetRuntimeClassName method [Windows Runtime],IInputPaneInterop interface, GetRuntimeClassName method [Windows Runtime],IInspectable interface, IInputPaneInterop interface [Windows Runtime],GetRuntimeClassName method, IInputPaneInterop::GetRuntimeClassName, IInspectable interface [Windows Runtime],GetRuntimeClassName method, IInspectable.GetRuntimeClassName, IInspectable::GetRuntimeClassName, inspectable/IInputPaneInterop::GetRuntimeClassName, inspectable/IInspectable::GetRuntimeClassName, winrt.iinspectable_getruntimeclassname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInspectable::GetRuntimeClassName


## -description


Gets the fully qualified name of the current Windows Runtime object.


## -parameters




### -param className [out]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>*</b>

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

The caller is responsible for freeing the <i>className</i> string by using the <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a> function.   

The following table shows example class name strings that cold be returned by the <b>GetRuntimeClassName</b> method.


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
<td>Windows.Foundation.Collections.IVector`1&lt;Windows.Foundation.Collections.IMapâ€™2&lt;String, TailspinToys.IStore&gt;&gt;</td>
<td>A vector of maps of strings to TailspinToys.IStore interfaces. </td>
</tr>
</table>
 



The <b>GetRuntimeClassName</b> method provides the most specific type information that the server object guarantees that it implements. The type name may be a runtime class name, interface group name, interface name, or parameterized interface name. 

The <b>GetRuntimeClassName</b> method returns <b>E_ILLEGAL_METHOD_CALL</b> if the class name refers to a class factory or a static interface. 




## -see-also




<a href="https://msdn.microsoft.com/DAE4705C-B786-44D4-8B03-1523EFC4C190">IInputPaneInterop</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

