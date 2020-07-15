---
UID: NN:wmsdkidl.IWMDRMReader2
title: IWMDRMReader2 (wmsdkidl.h)
description: The IWMDRMReader2 interface provides methods for examining the rights granted by DRM version 10 licenses.An IWMDRMReader2 interface exists for every instance of the reader object.
helpviewer_keywords: ["IWMDRMReader2","IWMDRMReader2 interface [windows Media Format]","IWMDRMReader2 interface [windows Media Format]","described","IWMDRMReader2Interface","wmformat.iwmdrmreader2","wmsdkidl/IWMDRMReader2"]
old-location: wmformat\iwmdrmreader2.htm
tech.root: wmformat
ms.assetid: 9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05
ms.date: 12/05/2018
ms.keywords: IWMDRMReader2, IWMDRMReader2 interface [windows Media Format], IWMDRMReader2 interface [windows Media Format],described, IWMDRMReader2Interface, wmformat.iwmdrmreader2, wmsdkidl/IWMDRMReader2
f1_keywords:
- wmsdkidl/IWMDRMReader2
dev_langs:
- c++
req.header: wmsdkidl.h
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
- wmsdkidl.h
api_name:
- IWMDRMReader2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMReader2 interface


## -description


<p class="CCE_Message">[<b>IWMDRMReader2</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMReader2</b> interface provides methods for examining the rights granted by DRM version 10 licenses.

An <b>IWMDRMReader2</b> interface exists for every instance of the reader object. You can get a pointer to this method by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMReader2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader</a>. <b>IWMDRMReader2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMReader2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels">GetCopyOutputLevels</a>
</td>
<td align="left" width="63%">
Retrieves the output protection levels that apply to the copy action in the license of the file loaded in the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels">GetPlayOutputLevels</a>
</td>
<td align="left" width="63%">
Retrieves the output protection levels that apply to the play action in the license of the file loaded in the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses">SetEvaluateOutputLevelLicenses</a>
</td>
<td align="left" width="63%">
Sets the reader to evaluate licenses that use output protection levels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense">TryNextLicense</a>
</td>
<td align="left" width="63%">
Sets the reader to evaluate the next applicable license for the file loaded in the player.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader3">IWMDRMReader3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

