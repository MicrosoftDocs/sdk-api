---
UID: NF:comsvcs.IHolder.UntrackResource
title: IHolder::UntrackResource
author: windows-sdk-content
description: Stops tracking a resource.
old-location: cos\iholder_untrackresource.htm
tech.root: cossdk
ms.assetid: 380b09ad-08d6-4d25-8d80-0e56d4295b8f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IHolder interface [COM+],UntrackResource method, IHolder.UntrackResource, IHolder::UntrackResource, UntrackResource, UntrackResource method [COM+], UntrackResource method [COM+],IHolder interface, _dtc_IHolder_UntrackResource, comsvcs/IHolder::UntrackResource, cos.iholder_untrackresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ComSvcs.h
api_name:
 - IHolder.UntrackResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHolder::UntrackResource


## -description


Stops tracking a resource.


## -parameters




### -param __MIDL__IHolder0005

TBD


### -param __MIDL__IHolder0006

TBD




#### - ResId [in]

The handle of the resource to stop tracking.


#### - fDestroy [in]

If <b>TRUE</b>, caller is requesting that the resource be destroyed, by calling <a href="https://msdn.microsoft.com/94e3e340-7dde-4b7f-82a9-83cd2400bde5">IDispenserDriver::DestroyResource</a>. If <b>FALSE</b>, caller destroys the resource.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ResId</i> is not a valid resource handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL </b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>



<a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a>
 

 

