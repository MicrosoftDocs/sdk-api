---
UID: NF:dshowasf.IConfigAsfWriter.ConfigureFilterUsingProfile
title: IConfigAsfWriter::ConfigureFilterUsingProfile
author: windows-sdk-content
description: The ConfigureFilterUsingProfile method sets an ASF profile on the WM ASF Writer filter. This method is the recommended way to set a profile on the WM ASF Writer filter.
old-location: dshow\iconfigasfwriter_configurefilterusingprofile.htm
old-project: DirectShow
ms.assetid: 89156f64-7a20-4226-9f01-5b1bd4a1fe98
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ConfigureFilterUsingProfile, ConfigureFilterUsingProfile method [DirectShow], ConfigureFilterUsingProfile method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],ConfigureFilterUsingProfile method, IConfigAsfWriter.ConfigureFilterUsingProfile, IConfigAsfWriter::ConfigureFilterUsingProfile, IConfigAsfWriterConfigureFilterUsingProfile, dshow.iconfigasfwriter_configurefilterusingprofile, dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfile
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
 - IConfigAsfWriter.ConfigureFilterUsingProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IConfigAsfWriter::ConfigureFilterUsingProfile


## -description



The <code>ConfigureFilterUsingProfile</code> method sets an ASF profile on the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter. This method is the recommended way to set a profile on the WM ASF Writer filter.




## -parameters




### -param pProfile [in]

Pointer to the <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface of the profile.


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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The graph is stopped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface pointer is invalid.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface is documented in the Windows Media Format SDK.

If successful, this method will cause an <a href="https://msdn.microsoft.com/621591d2-74ac-4b1f-b065-247582b05efc">EC_GRAPH_CHANGED</a> event to be sent to the application.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter Interface</a>
 

 

