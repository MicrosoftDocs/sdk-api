---
UID: NF:comsvcs.IHolder.UntrackResourceS
title: IHolder::UntrackResourceS
author: windows-sdk-content
description: Stops tracking a resource (string version).
old-location: cos\iholder_untrackresources.htm
old-project: cossdk
ms.assetid: 03e54d2d-9dfb-46cf-abb9-d3f37784c449
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IHolder interface [COM+],UntrackResourceS method, IHolder.UntrackResourceS, IHolder::UntrackResourceS, UntrackResourceS, UntrackResourceS method [COM+], UntrackResourceS method [COM+],IHolder interface, _dtc_IHolder_UntrackResourceS, comsvcs/IHolder::UntrackResourceS, cos.iholder_untrackresources
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IHolder.UntrackResourceS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IHolder::UntrackResourceS


## -description


Stops tracking a resource (string version).


## -parameters




### -param __MIDL__IHolder0007




### -param __MIDL__IHolder0008






#### - SResId [in]

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
<i>SResId</i> is not a valid resource handle.

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
 

 

