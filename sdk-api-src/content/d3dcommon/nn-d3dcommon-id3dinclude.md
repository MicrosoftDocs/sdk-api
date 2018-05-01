---
UID: NN:d3dcommon.ID3DInclude
title: ID3DInclude
author: windows-driver-content
description: ID3DInclude is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader #include files.
old-location: direct3d11\id3dinclude.htm
old-project: direct3d11
ms.assetid: 2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3DInclude, ID3DInclude interface [Direct3D 11], ID3DInclude interface [Direct3D 11], described, d3dcommon/ID3DInclude, direct3d11.id3dinclude
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3dcommon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D_SHADER_VARIABLE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3DCompiler_47.dll
api_name:
-	ID3DInclude
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3DInclude interface


## -description


<b>ID3DInclude</b> is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader #include files.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3DInclude</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3DInclude</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3DInclude</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
A user-implemented method for closing a shader #include file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
A user-implemented method for opening and reading the contents of a shader #include file.

</td>
</tr>
</table> 


## -remarks




          To use this interface, create an interface that inherits from <b>ID3DInclude</b> and implement custom behavior for the methods.
        




## -see-also




<a href="https://msdn.microsoft.com/d228c3c2-e2ff-4723-aec1-5c3ce82c321d">Common Version Interfaces</a>
 

 

