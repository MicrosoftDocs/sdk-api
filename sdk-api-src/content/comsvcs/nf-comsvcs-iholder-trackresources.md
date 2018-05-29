---
UID: NF:comsvcs.IHolder.TrackResourceS
title: IHolder::TrackResourceS
author: windows-sdk-content
description: Tracks the resource (string version).
old-location: cos\iholder_trackresources.htm
old-project: cossdk
ms.assetid: 1971820f-49aa-455d-a533-1a88fd8c28b8
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IHolder interface [COM+],TrackResourceS method, IHolder.TrackResourceS, IHolder::TrackResourceS, TrackResourceS, TrackResourceS method [COM+], TrackResourceS method [COM+],IHolder interface, _dtc_IHolder_TrackResourceS, comsvcs/IHolder::TrackResourceS, cos.iholder_trackresources
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IHolder.TrackResourceS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IHolder::TrackResourceS


## -description


Tracks the resource (string version).


## -parameters




### -param __MIDL__IHolder0004






#### - SResId [in]

The handle of the resource to be tracked. The Resource Dispenser has already created this resource before calling <b>TrackResourceS</b>.


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
The method failed. The resource has not been tracked. The likely cause is that the caller's transaction is aborting.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>



<a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a>
 

 

