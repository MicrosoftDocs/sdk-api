---
UID: NF:d3d11_1.ID3D11Device1.GetImmediateContext1
title: ID3D11Device1::GetImmediateContext1 method
author: windows-driver-content
description: Gets an immediate context, which can play back command lists.
old-location: direct3d11\id3d11device1_getimmediatecontext1.htm
old-project: direct3d11
ms.assetid: E66CDC7E-21B5-4675-A7A1-6F94940A4C13
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: GetImmediateContext1 method [Direct3D 11], GetImmediateContext1 method [Direct3D 11], ID3D11Device1 interface, GetImmediateContext1,ID3D11Device1.GetImmediateContext1, ID3D11Device1, ID3D11Device1 interface [Direct3D 11], GetImmediateContext1 method, ID3D11Device1::GetImmediateContext1, d3d11_1/ID3D11Device1::GetImmediateContext1, direct3d11.id3d11device1_getimmediatecontext1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Device1.GetImmediateContext1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device1::GetImmediateContext1 method


## -description


Gets an immediate context, which can play back command lists.


## -parameters




### -param ppImmediateContext [out]

Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a> interface pointer is initialized.


## -returns



This method does not return a value.




## -remarks



<b>GetImmediateContext1</b> returns an <a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a> object that represents an immediate context. You can use this immediate context to perform rendering that you want immediately submitted to a device. For most applications, an immediate context is the primary object that is used to draw your scene.

<b>GetImmediateContext1</b> increments the reference count of the immediate context by one. So, call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.






## -see-also




<a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>
 

 

