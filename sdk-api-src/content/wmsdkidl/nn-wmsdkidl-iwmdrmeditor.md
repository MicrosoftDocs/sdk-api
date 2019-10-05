---
UID: NN:wmsdkidl.IWMDRMEditor
title: IWMDRMEditor (wmsdkidl.h)
author: windows-sdk-content
description: The IWMDRMEditor interface is exposed on the metadata editor object.
old-location: wmformat\iwmdrmeditor.htm
tech.root: wmformat
ms.assetid: a404d30d-0b42-44c9-93e6-3eb9ef9e40fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDRMEditor, IWMDRMEditor interface [windows Media Format], IWMDRMEditor interface [windows Media Format],described, IWMDRMEditorInterface, wmformat.iwmdrmeditor, wmsdkidl/IWMDRMEditor
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMDRMEditor"
dev_langs:
 - c++
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IWMDRMEditor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMEditor interface


## -description


<p class="CCE_Message">[<b>IWMDRMEditor</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMEditor</b> interface is exposed on the metadata editor object. It can be obtained by calling <b>QueryInterface</b> from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor</a>. The <b>IWMDRMEditor</b> interface enables applications to examine the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">DRM</a> attributes of an ASF file, for example to query the number of times a file is allowed to be played, without having the wmstubdrm.lib static library. The <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader</a> interface contains a similar method, but the application must be linked to a valid wmstubdrm.lib library in order to use that interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMEditor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMEditor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMEditor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty">GetDRMProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified DRM property or file attribute.

</td>
</tr>
</table> 

For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty">IWMDRMReader::GetDRMProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/viewing-attributes-of-protected-files">Viewing Attributes of Protected Files</a>
 

 

