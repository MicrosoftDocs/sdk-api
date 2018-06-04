---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IIsoImageManager::Validate


## -description


Determines if the provided .iso image is valid.


## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</b></dt>
</dl>
</td>
<td width="60%">
The image is not aligned on a 2kb sector boundary.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The image does not contain a valid volume descriptor.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_NO_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The image has not been set using the <a href="https://msdn.microsoft.com/3e5ef908-795d-4617-8123-605855b9ddc8">SetPath</a> or <a href="https://msdn.microsoft.com/3ee540aa-8ccc-40cb-afc8-b1790cabee6e">SetStream</a> method prior to calling this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</b></dt>
</dl>
</td>
<td width="60%">
The provided image is too large to be validated as the size exceeds MAXLONG.

</td>
</tr>
</table>
 




## -remarks



For this method to succeed, the disc image, which may be a file or a stream, must meet the following criteria:<ul>
<li>The disc image size must be a multiple of the sector user data size, 2048 bytes.</li>
<li>The disc image must contain user data only and no sector header or file header.</li>
<li>The disc image must contain a valid Volume Recognition Sequence with at least one Volume Descriptor such as described in ECMA <a href="http://go.microsoft.com/fwlink/p/?linkid=149380">119</a>, <a href="http://go.microsoft.com/fwlink/p/?linkid=149381">167</a>, <a href="http://go.microsoft.com/fwlink/p/?linkid=149382">168</a> standards.</li>
</ul> 
 
If the disc image does not fit these criteria, this method will return the relevant failure code. More importantly, a failure to validate will affect the probability of operation success when the image is mounted by Windows after recording.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/47b059a9-a18a-4f32-9a02-6566175ca86b">IIsoImageManager</a>
 

 

