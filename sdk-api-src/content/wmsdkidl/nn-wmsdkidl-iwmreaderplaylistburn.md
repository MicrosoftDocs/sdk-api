---
UID: NN:wmsdkidl.IWMReaderPlaylistBurn
title: IWMReaderPlaylistBurn (wmsdkidl.h)
description: The IWMReaderPlaylistBurn interface verifies that the files in a playlist can be copied to CD, in the order in which they are specified.
helpviewer_keywords: ["IWMReaderPlaylistBurn","IWMReaderPlaylistBurn interface [windows Media Format]","IWMReaderPlaylistBurn interface [windows Media Format]","described","IWMReaderPlaylistBurnInterface","wmformat.iwmreaderplaylistburn","wmsdkidl/IWMReaderPlaylistBurn"]
old-location: wmformat\iwmreaderplaylistburn.htm
tech.root: wmformat
ms.assetid: a0e1a4f3-4226-44a2-b38e-e5512fda2048
ms.date: 12/05/2018
ms.keywords: IWMReaderPlaylistBurn, IWMReaderPlaylistBurn interface [windows Media Format], IWMReaderPlaylistBurn interface [windows Media Format],described, IWMReaderPlaylistBurnInterface, wmformat.iwmreaderplaylistburn, wmsdkidl/IWMReaderPlaylistBurn
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
 - IWMReaderPlaylistBurn
 - wmsdkidl/IWMReaderPlaylistBurn
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
 - IWMReaderPlaylistBurn
---

# IWMReaderPlaylistBurn interface


## -description

The <b>IWMReaderPlaylistBurn</b> interface verifies that the files in a playlist can be copied to CD, in the order in which they are specified. If any of the files in the list are DRM-protected, the licenses are checked. DRM version 10 licenses track the number of times files are copied to CD as part of a playlist. The methods of this interface are intended to support applications that copy entire playlists to compact disc.

An <b>IWMReaderPlaylistBurn</b> interface exists for every instance of the reader object or synchronous reader object. You can get a pointer to the <b>IWMReaderPlaylistBurn</b> interface by calling the <b>QueryInterface</b> method of any other interface on one of those objects.

## -inheritance

The <b>IWMReaderPlaylistBurn</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderPlaylistBurn</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
