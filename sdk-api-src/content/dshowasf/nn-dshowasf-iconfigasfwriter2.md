---
UID: NN:dshowasf.IConfigAsfWriter2
title: IConfigAsfWriter2 (dshowasf.h)
description: The IConfigAsfWriter2 interface extends the IConfigAsfWriter interface, which configures the WM ASF Writer filter.
helpviewer_keywords: ["IConfigAsfWriter2","IConfigAsfWriter2 interface [DirectShow]","IConfigAsfWriter2 interface [DirectShow]","described","IConfigAsfWriter2Interface","dshow.iconfigasfwriter2","dshowasf/IConfigAsfWriter2"]
old-location: dshow\iconfigasfwriter2.htm
tech.root: dshow
ms.assetid: fd931a95-3678-46de-8f17-9e7c27087398
ms.date: 12/05/2018
ms.keywords: IConfigAsfWriter2, IConfigAsfWriter2 interface [DirectShow], IConfigAsfWriter2 interface [DirectShow],described, IConfigAsfWriter2Interface, dshow.iconfigasfwriter2, dshowasf/IConfigAsfWriter2
f1_keywords:
- dshowasf/IConfigAsfWriter2
dev_langs:
- c++
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
- IConfigAsfWriter2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConfigAsfWriter2 interface


## -description



The <code>IConfigAsfWriter2</code> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter</a> interface, which configures the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. The <code>IConfigAsfWriter2</code> interface provides additional methods to support the capabilities introduced in the Windows Media Format 9 Series SDK, such as two-pass encoding and support for interlaced output.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConfigAsfWriter2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter</a>. <b>IConfigAsfWriter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConfigAsfWriter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter2-getparam">GetParam</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the specified filter configuration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate">ResetMultiPassState</a>
</td>
<td align="left" width="63%">
Resets the filter when a preprocessing encoding pass is canceled before it is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter2-setparam">SetParam</a>
</td>
<td align="left" width="63%">
Sets the value of the specified filter configuration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter2-streamnumfrompin">StreamNumFromPin</a>
</td>
<td align="left" width="63%">
Retrieves the stream number associated with the specified input pin.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter</a>
 

 

