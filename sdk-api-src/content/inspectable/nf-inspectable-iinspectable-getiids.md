---
UID: NF:inspectable.IInspectable.GetIids
title: IInspectable::GetIids
author: windows-sdk-content
description: Gets the interfaces that are implemented by the current Windows Runtime class.
old-location: winrt\iinspectable_getiids.htm
tech.root: WinRT
ms.assetid: 560094E6-3ED2-4BF3-85C7-07736ECBACC8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIids, GetIids method [Windows Runtime], GetIids method [Windows Runtime],IInputPaneInterop interface, GetIids method [Windows Runtime],IInspectable interface, IInputPaneInterop interface [Windows Runtime],GetIids method, IInputPaneInterop::GetIids, IInspectable interface [Windows Runtime],GetIids method, IInspectable.GetIids, IInspectable::GetIids, inspectable/IInputPaneInterop::GetIids, inspectable/IInspectable::GetIids, winrt.iinspectable_getiids
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
 - IInspectable.GetIids
 - IInputPaneInterop.GetIids
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInspectable::GetIids


## -description


Gets the interfaces that are implemented by the current Windows Runtime class.


## -parameters




### -param iidCount [out]

Type: <b>ULONG*</b>

The number of interfaces that are implemented by the current Windows Runtime object, excluding the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> implementations.


### -param iids [out]

Type: <b>IID**</b>

A pointer to an array that contains an IID for   each interface implemented by the current Windows Runtime object. The <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interfaces are excluded.


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
The  <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate <i>iids</i>.

</td>
</tr>
</table>
 




## -remarks



Use the <b>GetIids</b> method to discover the interfaces that are implemented by a Windows Runtime object.

A <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call on any IID in the <i>iids</i> array must succeed.

The caller is responsible for freeing the IID array by using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/DAE4705C-B786-44D4-8B03-1523EFC4C190">IInputPaneInterop</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

