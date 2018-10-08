---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetVertexProcessing
title: ID2D1DrawInfo::SetVertexProcessing
author: windows-sdk-content
description: Sets a vertex buffer, a corresponding vertex shader, and options to control how the vertices are to be handled by the Direct2D context.
old-location: direct2d\id2d1drawinfo_setvertexprocessing.htm
tech.root: Direct2D
ms.assetid: 23DB679B-33E4-4FB1-B356-BBB1BA95E0EB
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetVertexProcessing method, ID2D1DrawInfo.SetVertexProcessing, ID2D1DrawInfo::SetVertexProcessing, SetVertexProcessing, SetVertexProcessing method [Direct2D], SetVertexProcessing method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetVertexProcessing, direct2d.id2d1drawinfo_setvertexprocessing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1DrawInfo.SetVertexProcessing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawInfo::SetVertexProcessing


## -description


Sets a vertex buffer, a corresponding vertex shader, and options to control how the vertices are to be handled by the Direct2D context.


## -parameters




### -param vertexBuffer [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1DBCDF93-83C6-4B02-9E94-8024D7849DF7">ID2D1VertexBuffer</a>*</b>

The vertex buffer, if this is cleared, the default vertex shader and mapping to the transform rectangles will be used.


### -param vertexOptions

Type: <b><a href="https://msdn.microsoft.com/b308aaf4-edf0-49a8-8fbf-04bb38c00605">D2D1_VERTEX_OPTIONS</a></b>

Options that influence how the renderer will interact with the vertex shader.


### -param blendDescription [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/5f4c7248-9303-4451-92f1-4b230efd627a">D2D1_BLEND_DESCRIPTION</a>*</b>

How the vertices will be blended with the output texture.


### -param vertexRange [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a5c93541-86dd-48d3-b731-50e9f66f401d">D2D1_VERTEX_RANGE</a>*</b>

The set of vertices to use from the buffer.



### -param vertexShader

Type: <b>GUID*</b>

The GUID of the vertex shader.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The vertex shaders associated with the vertex buffer through the vertex shader GUID must have been loaded through the <a href="https://msdn.microsoft.com/60D3DB1B-D347-44FC-98F9-545D4213F1F0">ID2D1EffectContext::LoadVertexShader</a> method before this call is made.

If you pass the vertex option <a href="https://msdn.microsoft.com/b308aaf4-edf0-49a8-8fbf-04bb38c00605">D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR</a>, then the method fails unless the blend description is exactly this:



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>D2D1_BLEND_DESCRIPTION blendDesc = 
        {
            D2D1_BLEND_ONE,
            D2D1_BLEND_ZERO,
            D2D1_BLEND_OPERATION_ADD,

            D2D1_BLEND_ONE,
            D2D1_BLEND_ZERO,
            D2D1_BLEND_OPERATION_ADD,

            { 1.0f, 1.0f, 1.0f, 1.0f }
        };</pre>
</td>
</tr>
</table></span></div>
If this call fails, the corresponding <a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a> instance is placed into an error state and fails to draw.

  If blendDescription is NULL, a foreground-over blend mode is used.




## -see-also




<a href="https://msdn.microsoft.com/9C7B8CE0-0D2D-4383-9BE1-25F86BCEF253">ID2D1DrawInfo</a>



<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/60D3DB1B-D347-44FC-98F9-545D4213F1F0">ID2D1EffectContext::LoadVertexShader</a>
 

 

