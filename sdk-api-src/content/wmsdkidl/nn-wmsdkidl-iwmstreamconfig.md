---
UID: NN:wmsdkidl.IWMStreamConfig
title: IWMStreamConfig (wmsdkidl.h)
description: The IWMStreamConfig interface is the primary interface of a stream configuration object.
helpviewer_keywords: ["IWMStreamConfig","IWMStreamConfig interface [windows Media Format]","IWMStreamConfig interface [windows Media Format]","described","IWMStreamConfigInterface","wmformat.iwmstreamconfig","wmsdkidl/IWMStreamConfig"]
old-location: wmformat\iwmstreamconfig.htm
tech.root: wmformat
ms.assetid: e013996a-95b6-4cd3-9fb5-75dbce821eef
ms.date: 4/26/2023
ms.keywords: IWMStreamConfig, IWMStreamConfig interface [windows Media Format], IWMStreamConfig interface [windows Media Format],described, IWMStreamConfigInterface, wmformat.iwmstreamconfig, wmsdkidl/IWMStreamConfig
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
 - IWMStreamConfig
 - wmsdkidl/IWMStreamConfig
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
 - IWMStreamConfig
---

# IWMStreamConfig interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMStreamConfig</b> interface is the primary interface of a stream configuration object. It provides methods to configure basic properties for streams to be used in a profile.

Every profile contains one or more stream configuration objects. You can get the <b>IWMStreamConfig</b> interface of a stream configuration object by calling the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a> method or the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">IWMProfile::GetStreamByNumber</a> method. The difference between these two methods is that <b>GetStream</b> retrieves the stream using an index ranging from zero to one less than the total stream count, and <b>GetStreamByNumber</b> retrieves the stream using the assigned stream number. You can also retrieve a stream configuration object using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream">IWMProfile::CreateNewStream</a> method. All of the methods that create stream configuration objects set a pointer to this interface.

<div class="alert"><b>Important</b>  After calling one or more of the <b>IWMStreamConfig::Set...</b> methods, you must call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a> for all the changes to take effect in the profile.</div>
<div> </div>

## -inheritance

The <b>IWMStreamConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStreamConfig</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps Interface</a>



<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3">IWMStreamConfig3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>
