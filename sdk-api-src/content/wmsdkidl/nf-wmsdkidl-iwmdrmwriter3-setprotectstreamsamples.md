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

# IWMDRMWriter3::SetProtectStreamSamples


## -description


<p class="CCE_Message">[<b>SetProtectStreamSamples</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>SetProtectStreamSamples</b> method configures the writer to accept encrypted stream samples. This method is used as part of the process of importing protected content from a third party content protection scheme (CPS) into Windows Media DRM.




## -parameters




### -param pImportInitStruct [in]

Address of a <a href="https://msdn.microsoft.com/191b844e-5760-44d7-9b27-9fa87fead90f">WMDRM_IMPORT_INIT_STRUCT</a> structure containing initialization information needed to import protected content.


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
<dt><b>NS_E_DRM_RIV_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
An updated content revocation list is needed.

</td>
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



<b>SetProtectStreamSamples</b> is used to configure the writer object for importing protected content.

When importing protected content, this method must be called after configuring the writer but before calling <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a>. Before you can call this method, you must validate and extract the machine Windows Media DRM public key from the machine certificate collection.




## -see-also




<a href="https://msdn.microsoft.com/5e67a721-830b-4d99-9f90-4cb2d7c61104">DRM Import</a>



<a href="https://msdn.microsoft.com/38b8e812-e997-4a63-b906-ebd26a5556be">IWMDRMSecurity::GetMachineCertificate</a>



<a href="https://msdn.microsoft.com/e450a1e3-6024-4c00-9978-fbc88fde2101">IWMDRMSecurity::PerformSecurityUpdate</a>



<a href="https://msdn.microsoft.com/b300b97b-e558-4c33-a84a-e92c28a3a606">IWMDRMWriter3 Interface</a>
 

 

