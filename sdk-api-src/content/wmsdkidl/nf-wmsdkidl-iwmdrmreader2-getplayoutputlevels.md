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

# IWMDRMReader2::GetPlayOutputLevels


## -description


<p class="CCE_Message">[<b>GetPlayOutputLevels</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>GetPlayOutputLevels</b> method retrieves the output protection levels (OPLs) that apply to the play action in the license of the file loaded in the reader.




## -parameters




### -param pPlayOPL [out]

Address of a <a href="https://msdn.microsoft.com/5d14bd02-0fb5-4982-b3dc-7f8277cb852f">DRM_PLAY_OPL</a> structure that receives the output levels that apply to playing content. Additional data is appended to the structure. If you pass <b>NULL</b>, the method returns the size of the structure in <i>pcbLength</i>.


### -param pcbLength [in, out]

Address of a variable that contains the size of the <b>DRM_PLAY_OPL</b> structure in bytes. On input set to the size of the allocated buffer. On return the method sets this value to the size of the structure and any appended data.


### -param pdwMinAppComplianceLevel [out]

Address of a variable that receives the minimum application compliance level.


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



When reading DRM-protected content, you must verify that the destination of the protected content is allowed by the license. Calling this method enables you to check the output protection level required by the license.

Before you call this method, you must call <a href="https://msdn.microsoft.com/5a146ec4-a733-483c-8b08-2bee0081bd96">SetEvaluateOutputLevelLicenses</a> to configure the reader to evaluate licenses that contain output protection levels.

If the OPL information returned by this method indicates that you cannot play the content using the desired technology, you can call <a href="https://msdn.microsoft.com/2658abd7-61ca-452f-92ad-93ee5050603d">TryNextLicense</a> to find out whether there is another license on the computer that you can use.




## -see-also




<a href="https://msdn.microsoft.com/9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05">IWMDRMReader2 Interface</a>



<a href="https://msdn.microsoft.com/32c8110b-1a96-432d-a82c-5769757dd4f6">IWMDRMReader2::GetCopyOutputLevels</a>
 

 

