---
UID: NN:wmsdkidl.IWMWriterPreprocess
title: IWMWriterPreprocess (wmsdkidl.h)
description: The IWMWriterPreprocess interface handles multi-pass encoding.helpviewer_keywords: ["IWMWriterPreprocess","IWMWriterPreprocess interface [windows Media Format]","IWMWriterPreprocess interface [windows Media Format]","described","IWMWriterPreprocessInterface","wmformat.iwmwriterpreprocess","wmsdkidl/IWMWriterPreprocess"]
old-location: wmformat\iwmwriterpreprocess.htm
tech.root: wmformat
ms.assetid: 06803639-3f21-4003-a460-16a0b5cc6d6f
ms.date: 12/05/2018
ms.keywords: IWMWriterPreprocess, IWMWriterPreprocess interface [windows Media Format], IWMWriterPreprocess interface [windows Media Format],described, IWMWriterPreprocessInterface, wmformat.iwmwriterpreprocess, wmsdkidl/IWMWriterPreprocess
f1_keywords:
- wmsdkidl/IWMWriterPreprocess
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMWriterPreprocess
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterPreprocess interface


## -description



The <b>IWMWriterPreprocess</b> interface handles multi-pass encoding. By making more than one pass, the writer can obtain better quality with better compression.

An <b>IWMWriterPreprocess</b> interface exists for every instance of the writer object. You can obtain a pointer to <b>IWMWriterPreprocess</b> with a call to the <b>QueryInterface</b> method of any other interface in the writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPreprocess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriterPreprocess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterPreprocess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpreprocess-beginpreprocessingpass">BeginPreprocessingPass</a>
</td>
<td align="left" width="63%">
Begins preprocessing a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpreprocess-endpreprocessingpass">EndPreprocessingPass</a>
</td>
<td align="left" width="63%">
Ends preprocessing a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpreprocess-getmaxpreprocessingpasses">GetMaxPreprocessingPasses</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of preprocessing passes supported for a specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpreprocess-preprocesssample">PreprocessSample</a>
</td>
<td align="left" width="63%">
Retrieves a sample for preprocessing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpreprocess-setnumpreprocessingpasses">SetNumPreprocessingPasses</a>
</td>
<td align="left" width="63%">
Sets the number of preprocessing passes to perform.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/using-two-pass-encoding">Using Two-Pass Encoding</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

