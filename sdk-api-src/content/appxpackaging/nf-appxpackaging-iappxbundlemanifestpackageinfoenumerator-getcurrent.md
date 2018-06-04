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

# IAppxBundleManifestPackageInfoEnumerator::GetCurrent


## -description


Gets the &lt;Package&gt; element at the current position of the enumerator.


## -parameters




### -param packageInfo [out, retval]

Type: <b><a href="https://msdn.microsoft.com/B9272875-E02A-4443-82B3-C64104E8291C">IAppxBundleManifestPackageInfo</a>**</b>

The current &lt;Package&gt; element. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has passed the last item in the collection.

</td>
</tr>
</table>
 




## -remarks



The enumerator’s position points to the first element by default. So, with a newly constructed enumerator that contains at least one element, <a href="https://msdn.microsoft.com/ED12F498-1F8D-45B2-9CFE-7215D2D87C3F">IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent</a> returns <b>TRUE</b> and <b>GetCurrent</b> returns the first element.




## -see-also




<a href="https://msdn.microsoft.com/4861D5CF-9FDC-4BAA-8462-D239DAEB5195">IAppxBundleManifestPackageInfoEnumerator</a>
 

 

