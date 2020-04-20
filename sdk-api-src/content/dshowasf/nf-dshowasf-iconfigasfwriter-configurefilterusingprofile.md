---
UID: NF:dshowasf.IConfigAsfWriter.ConfigureFilterUsingProfile
title: IConfigAsfWriter::ConfigureFilterUsingProfile (dshowasf.h)
description: The ConfigureFilterUsingProfile method sets an ASF profile on the WM ASF Writer filter. This method is the recommended way to set a profile on the WM ASF Writer filter.helpviewer_keywords: ["ConfigureFilterUsingProfile","ConfigureFilterUsingProfile method [DirectShow]","ConfigureFilterUsingProfile method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","ConfigureFilterUsingProfile method","IConfigAsfWriter.ConfigureFilterUsingProfile","IConfigAsfWriter::ConfigureFilterUsingProfile","IConfigAsfWriterConfigureFilterUsingProfile","dshow.iconfigasfwriter_configurefilterusingprofile","dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfile"]
old-location: dshow\iconfigasfwriter_configurefilterusingprofile.htm
tech.root: DirectShow
ms.assetid: 89156f64-7a20-4226-9f01-5b1bd4a1fe98
ms.date: 12/05/2018
ms.keywords: ConfigureFilterUsingProfile, ConfigureFilterUsingProfile method [DirectShow], ConfigureFilterUsingProfile method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],ConfigureFilterUsingProfile method, IConfigAsfWriter.ConfigureFilterUsingProfile, IConfigAsfWriter::ConfigureFilterUsingProfile, IConfigAsfWriterConfigureFilterUsingProfile, dshow.iconfigasfwriter_configurefilterusingprofile, dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfile
f1_keywords:
- dshowasf/IConfigAsfWriter.ConfigureFilterUsingProfile
dev_langs:
- c++
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
- IConfigAsfWriter.ConfigureFilterUsingProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConfigAsfWriter::ConfigureFilterUsingProfile


## -description



The <code>ConfigureFilterUsingProfile</code> method sets an ASF profile on the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. This method is the recommended way to set a profile on the WM ASF Writer filter.




## -parameters




### -param pProfile [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface of the profile.


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
The <a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface pointer is invalid.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface is documented in the Windows Media Format SDK.

If successful, this method will cause an <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-graph-changed">EC_GRAPH_CHANGED</a> event to be sent to the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>
 

 

