---
UID: NF:dshowasf.IConfigAsfWriter.ConfigureFilterUsingProfileGuid
title: IConfigAsfWriter::ConfigureFilterUsingProfileGuid
author: windows-sdk-content
description: The ConfigureFilterUsingProfileGuid method sets a predefined system profile on the WM ASF Writer filter. This method is deprecated. Applications should use the IConfigAsfWriter::ConfigureFilterUsingProfile method to set the profile.
old-location: dshow\iconfigasfwriter_configurefilterusingprofileguid.htm
old-project: DirectShow
ms.assetid: 8cfb3b22-aa6b-42e0-bbb5-876932e8bd82
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: ConfigureFilterUsingProfileGuid, ConfigureFilterUsingProfileGuid method [DirectShow], ConfigureFilterUsingProfileGuid method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],ConfigureFilterUsingProfileGuid method, IConfigAsfWriter.ConfigureFilterUsingProfileGuid, IConfigAsfWriter::ConfigureFilterUsingProfileGuid, IConfigAsfWriterConfigureFilterUsingProfileGuid, dshow.iconfigasfwriter_configurefilterusingprofileguid, dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileGuid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter.ConfigureFilterUsingProfileGuid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IConfigAsfWriter::ConfigureFilterUsingProfileGuid


## -description



The <code>ConfigureFilterUsingProfileGuid</code> method sets a predefined system profile on the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter. This method is deprecated. Applications should use the <a href="https://msdn.microsoft.com/89156f64-7a20-4226-9f01-5b1bd4a1fe98">IConfigAsfWriter::ConfigureFilterUsingProfile</a> method to set the profile.




## -parameters




### -param guidProfile [in]

Profile <b>GUID</b> as defined in the header file Wmsysprf.h.


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



Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined. Only version 8 (or earlier) system profile GUIDs can be used with this method.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter Interface</a>
 

 

