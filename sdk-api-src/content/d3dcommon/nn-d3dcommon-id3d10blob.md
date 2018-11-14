---
UID: NN:d3dcommon.ID3D10Blob
title: ID3D10Blob
author: windows-sdk-content
description: This interface is used to return arbitrary-length data.
old-location: direct3d11\id3d10blob.htm
tech.root: direct3d11
ms.assetid: 7E97B8EB-E674-4B90-9B9B-202552DBD95C
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D10Blob, ID3D10Blob interface [Direct3D 11], ID3D10Blob interface [Direct3D 11],described, d3dcommon/ID3D10Blob, direct3d11.id3d10blob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3dcommon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcommon.h
api_name:
 - ID3D10Blob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Blob interface


## -description


This interface is used to return arbitrary-length data.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Blob</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10Blob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Blob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21ABCED3-388E-41AD-B557-DA8707128B01">GetBufferPointer</a>
</td>
<td align="left" width="63%">
Gets a pointer to the data.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E98833B1-07F7-4015-86C6-B9335529FC29">GetBufferSize</a>
</td>
<td align="left" width="63%">
Gets the size.
        

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface is type-defined in the D3DCommon.h header file as a <b>ID3D10Blob</b> interface, which is fully defined in the D3DCommon.h header file.
          <b>ID3DBlob</b> is version-neutral and can be used in code for any Direct3D version.
        

Blobs can be used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.
          Also, these objects are used to return object code and error messages in APIs that compile vertex, geometry and pixel shaders.
        




## -see-also




<a href="https://msdn.microsoft.com/d228c3c2-e2ff-4723-aec1-5c3ce82c321d">Common Version Interfaces</a>



<a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

