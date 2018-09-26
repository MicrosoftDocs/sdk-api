---
UID: NF:dshowasf.IConfigAsfWriter.ConfigureFilterUsingProfileId
title: IConfigAsfWriter::ConfigureFilterUsingProfileId
author: windows-sdk-content
description: The ConfigureFilterUsingProfileId method sets a Windows Media Format 4.0 profile on the WM ASF Writer filter. This method is deprecated. Applications should use the IConfigAsfWriter::ConfigureFilterUsingProfile method to set the profile.
old-location: dshow\iconfigasfwriter_configurefilterusingprofileid.htm
tech.root: DirectShow
ms.assetid: e532001a-e2ff-4ad4-8fef-2fa5b051d1f5
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ConfigureFilterUsingProfileId, ConfigureFilterUsingProfileId method [DirectShow], ConfigureFilterUsingProfileId method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],ConfigureFilterUsingProfileId method, IConfigAsfWriter.ConfigureFilterUsingProfileId, IConfigAsfWriter::ConfigureFilterUsingProfileId, IConfigAsfWriterConfigureFilterUsingProfileId, dshow.iconfigasfwriter_configurefilterusingprofileid, dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Dshowasf.h
api_name:
 - IConfigAsfWriter.ConfigureFilterUsingProfileId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter::ConfigureFilterUsingProfileId


## -description



The <code>ConfigureFilterUsingProfileId</code> method sets a Windows Media Format 4.0 profile on the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter. This method is deprecated. Applications should use the <a href="https://msdn.microsoft.com/89156f64-7a20-4226-9f01-5b1bd4a1fe98">IConfigAsfWriter::ConfigureFilterUsingProfile</a> method to set the profile.




## -parameters




### -param dwProfileId [in]

Profile ID as defined in version 4.0 of the Windows Media Format SDK.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The profile is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is stopped.

</td>
</tr>
</table>
 




## -remarks



This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter Interface</a>
 

 

