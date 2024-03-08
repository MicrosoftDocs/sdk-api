---
UID: NN:wmsdkidl.IWMProfile3
title: IWMProfile3 (wmsdkidl.h)
description: The IWMProfile3 interface provides enhanced features for profiles.
helpviewer_keywords: ["IWMProfile3","IWMProfile3 interface [windows Media Format]","IWMProfile3 interface [windows Media Format]","described","IWMProfile3Interface","wmformat.iwmprofile3","wmsdkidl/IWMProfile3"]
old-location: wmformat\iwmprofile3.htm
tech.root: wmformat
ms.assetid: 7942aa81-ada7-4e9c-a261-f257f8f890b7
ms.date: 4/26/2023
ms.keywords: IWMProfile3, IWMProfile3 interface [windows Media Format], IWMProfile3 interface [windows Media Format],described, IWMProfile3Interface, wmformat.iwmprofile3, wmsdkidl/IWMProfile3
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
 - IWMProfile3
 - wmsdkidl/IWMProfile3
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
 - IWMProfile3
---

# IWMProfile3 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMProfile3</b> interface provides enhanced features for profiles. This includes the ability to create two new types of objects: bandwidth sharing objects and stream prioritization objects.

An <b>IWMProfile3</b> interface is created for each profile object created. You can retrieve a pointer to an <b>IWMProfile3</b> interface by calling the <b>QueryInterface</b> method of any other interface of the profile. You can also access <b>IWMProfile3</b> from a reader or synchronous reader object by calling the <b>QueryInterface</b> method of an existing interface in the object. For more information, see <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>.

## -inheritance

The <b>IWMProfile3</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>. <b>IWMProfile3</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing Interface</a>



<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/stream-prioritization-object">Stream Prioritization Object</a>
