---
UID: NN:dshowasf.IConfigAsfWriter
title: IConfigAsfWriter (dshowasf.h)
description: The IConfigAsfWriter interface configures the WM ASF Writer filter.
helpviewer_keywords: ["IConfigAsfWriter","IConfigAsfWriter interface [DirectShow]","IConfigAsfWriter interface [DirectShow]","described","IConfigAsfWriterInterface","dshow.iconfigasfwriter","dshowasf/IConfigAsfWriter"]
old-location: dshow\iconfigasfwriter.htm
tech.root: dshow
ms.assetid: 50fd7825-4844-4a7f-b949-4abfff5ef30f
ms.date: 12/05/2018
ms.keywords: IConfigAsfWriter, IConfigAsfWriter interface [DirectShow], IConfigAsfWriter interface [DirectShow],described, IConfigAsfWriterInterface, dshow.iconfigasfwriter, dshowasf/IConfigAsfWriter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigAsfWriter
 - dshowasf/IConfigAsfWriter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter
---

# IConfigAsfWriter interface


## -description

The <code>IConfigAsfWriter</code> interface configures the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. It provides methods for getting and setting the profiles and indexing mode.

When the WM ASF Writer filter is created, it is configured automatically with a default ASF audio-visual profile based on the incoming streams. A profile describes various attributes of an ASF file such as bit rate, number and type of streams, compression quality, and so on. The filter uses the profile to determine what kind of ASF file to write, how many input pins to create, and what media types to accept. When the WM ASF Writer filter is first created, it is configured automatically with the following default profile: WMProfile_V80_256Video. However, using this profile is not recommended because it does not use the Windows Media Audio and Video 9 Series codecs.

## -inheritance

The <b>IConfigAsfWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConfigAsfWriter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>
