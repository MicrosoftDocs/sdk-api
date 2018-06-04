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

# IWMDRMReader2::SetEvaluateOutputLevelLicenses


## -description


<p class="CCE_Message">[<b>SetEvaluateOutputLevelLicenses</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>SetEvaluateOutputLevelLicenses</b> method sets the reader to evaluate licenses that use output protection levels (OPLs).




## -parameters




### -param fEvaluate [in]

Flag specifying whether to handle files with licenses that use output protection levels.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If your application supports reading DRM-protected files with licenses that use output protection levels, you must call this method and set <i>fEvaluate</i> to <b>TRUE</b>. The call must be made before opening the file.

When a file is opened with OPL support enabled, you must call either <a href="https://msdn.microsoft.com/32c8110b-1a96-432d-a82c-5769757dd4f6">GetCopyOutputLevels</a> or <a href="https://msdn.microsoft.com/a53d58cc-655f-4441-9c16-5afc5b53a233">GetPlayOutputLevels</a>, depending on the actions your application performs. These methods provide minimum OPLs for the associated action.

If you do not call this method, the reader object will not open DRM-protected files that have licenses specifying output protection levels.




## -see-also




<a href="https://msdn.microsoft.com/9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05">IWMDRMReader2 Interface</a>
 

 

