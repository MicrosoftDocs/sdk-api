---
UID: NN:wmsdkidl.IWMWriterAdvanced
title: IWMWriterAdvanced (wmsdkidl.h)
description: The IWMWriterAdvanced interface provides advanced writing functionality.This interface exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
helpviewer_keywords: ["IWMWriterAdvanced","IWMWriterAdvanced interface [windows Media Format]","IWMWriterAdvanced interface [windows Media Format]","described","IWMWriterAdvancedInterface","wmformat.iwmwriteradvanced","wmsdkidl/IWMWriterAdvanced"]
old-location: wmformat\iwmwriteradvanced.htm
tech.root: wmformat
ms.assetid: 082cd277-157d-42a4-bf37-e47d16f90c7a
ms.date: 4/26/2023
ms.keywords: IWMWriterAdvanced, IWMWriterAdvanced interface [windows Media Format], IWMWriterAdvanced interface [windows Media Format],described, IWMWriterAdvancedInterface, wmformat.iwmwriteradvanced, wmsdkidl/IWMWriterAdvanced
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriterAdvanced
 - wmsdkidl/IWMWriterAdvanced
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMWriterAdvanced
---

# IWMWriterAdvanced interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriterAdvanced</b> interface provides advanced writing functionality.

This interface exists for every instance of the writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the writer object.

## -inheritance

The <b>IWMWriterAdvanced</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriterAdvanced</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2">IWMWriterAdvanced2 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>



<a href="/windows/desktop/wmformat/writing-asf-files">Writing ASF Files</a>
