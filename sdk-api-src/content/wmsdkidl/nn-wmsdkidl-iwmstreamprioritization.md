---
UID: NN:wmsdkidl.IWMStreamPrioritization
title: IWMStreamPrioritization (wmsdkidl.h)
description: The IWMStreamPrioritization interface provides methods to set and read priority records for a file.Stream prioritization allows content creators to specify the priority of the streams in an ASF file.
helpviewer_keywords: ["IWMStreamPrioritization","IWMStreamPrioritization interface [windows Media Format]","IWMStreamPrioritization interface [windows Media Format]","described","IWMStreamPrioritizationInterface","wmformat.iwmstreamprioritization","wmsdkidl/IWMStreamPrioritization"]
old-location: wmformat\iwmstreamprioritization.htm
tech.root: wmformat
ms.assetid: ef8ae275-c36a-492c-b57c-d640044ede93
ms.date: 4/26/2023
ms.keywords: IWMStreamPrioritization, IWMStreamPrioritization interface [windows Media Format], IWMStreamPrioritization interface [windows Media Format],described, IWMStreamPrioritizationInterface, wmformat.iwmstreamprioritization, wmsdkidl/IWMStreamPrioritization
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
 - IWMStreamPrioritization
 - wmsdkidl/IWMStreamPrioritization
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
 - IWMStreamPrioritization
---

# IWMStreamPrioritization interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMStreamPrioritization</b> interface provides methods to set and read priority records for a file.

Stream prioritization allows content creators to specify the priority of the streams in an ASF file. The streams assigned the lowest priority will be dropped first in the case of insufficient bit rate during playback.

Only one stream prioritization object can exist for a profile. You can check to see if one is present with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization">IWMProfile3::GetStreamPrioritization</a>, which will retrieve a pointer to one if it exists.

You can create a new stream prioritization object with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization">IWMProfile3::CreateNewStreamPrioritization</a>. You will then receive a pointer to <b>IWMStreamPrioritization</b> for the new object. This will erase the existing stream prioritization, if there is one.

## -inheritance

The <b>IWMStreamPrioritization</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStreamPrioritization</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/stream-prioritization-object">Stream Prioritization Object</a>
