---
UID: NF:d3d11_1.ID3D11DeviceContext1.DiscardView1
title: ID3D11DeviceContext1::DiscardView1
author: windows-sdk-content
description: Discards the specified elements in a resource view from the device context.
old-location: direct3d11\id3d11devicecontext1_discardview1.htm
old-project: direct3d11
ms.assetid: C478F696-D0D7-4ABB-8BCD-5C528CC13814
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DiscardView1, DiscardView1 method [Direct3D 11], DiscardView1 method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],DiscardView1 method, ID3D11DeviceContext1.DiscardView1, ID3D11DeviceContext1::DiscardView1, d3d11_1/ID3D11DeviceContext1::DiscardView1, direct3d11.id3d11devicecontext1_discardview1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext1.DiscardView1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext1::DiscardView1


## -description


Discards the specified elements in a resource view from the device context.


## -parameters




### -param pResourceView [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a> interface for the resource view to discard. The resource that underlies the view must have been created with usage <a href="https://msdn.microsoft.com/en-us/library/Ff476259(v=VS.85).aspx">D3D11_USAGE_DEFAULT</a> or <a href="https://msdn.microsoft.com/en-us/library/Ff476259(v=VS.85).aspx">D3D11_USAGE_DYNAMIC</a>, otherwise the runtime drops the call to <b>DiscardView1</b>; if the debug layer is enabled, the runtime returns an error message.
          


### -param pRects [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/d1cbbbd7-1221-4706-b805-8422c5ebdadc">D3D11_RECT</a>*</b>

An array of <a href="https://msdn.microsoft.com/d1cbbbd7-1221-4706-b805-8422c5ebdadc">D3D11_RECT</a> structures for the rectangles in the resource view to discard. If <b>NULL</b>, <b>DiscardView1</b> discards the entire view and behaves the same as <a href="https://msdn.microsoft.com/en-us/library/Hh404616(v=VS.85).aspx">DiscardView</a>.
          


### -param NumRects

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of rectangles in the array that the  <i>pRects</i> parameter specifies.
          


## -returns



Returns nothing




## -remarks



<b>DiscardView1</b> informs the graphics processing unit (GPU) that the existing content in the specified elements in the resource view that <i>pResourceView</i> points to is no longer needed.  The view can be an SRV, RTV, UAV, or DSV.  <b>DiscardView1</b> is a variation on the <a href="https://msdn.microsoft.com/en-us/library/Hh404613(v=VS.85).aspx">DiscardResource</a> method.  <b>DiscardView1</b> allows you to discard elements of a subset of a resource that is in a view (such as elements of a single miplevel).  More importantly, <b>DiscardView1</b> provides a convenience because often views are what are being bound and unbound at the pipeline.  Some pipeline bindings do not have views, such as stream output.  In that situation, <b>DiscardResource</b> can do the job for any resource.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404598(v=VS.85).aspx">ID3D11DeviceContext1</a>
 

 

