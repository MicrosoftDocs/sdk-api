---
UID: NN:wmsdkidl.IWMCodecInfo
title: IWMCodecInfo (wmsdkidl.h)
description: The IWMCodecInfo interface retrieves the number and types of codecs available.
helpviewer_keywords: ["IWMCodecInfo","IWMCodecInfo interface [windows Media Format]","IWMCodecInfo interface [windows Media Format]","described","IWMCodecInfoInterface","wmformat.iwmcodecinfo","wmsdkidl/IWMCodecInfo"]
old-location: wmformat\iwmcodecinfo.htm
tech.root: wmformat
ms.assetid: 70661d13-737a-4e83-94e6-9a1af07b0369
ms.date: 4/26/2023
ms.keywords: IWMCodecInfo, IWMCodecInfo interface [windows Media Format], IWMCodecInfo interface [windows Media Format],described, IWMCodecInfoInterface, wmformat.iwmcodecinfo, wmsdkidl/IWMCodecInfo
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
 - IWMCodecInfo
 - wmsdkidl/IWMCodecInfo
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
 - IWMCodecInfo
---

# IWMCodecInfo interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMCodecInfo</b> interface retrieves the number and types of codecs available. You can use this interface to get information about supported compressed data formats for creating custom profiles.

Individual codec formats exist only for audio codecs. The characteristics of compressed video will vary based upon the frame size and color depth of the original digital media and, therefore, cannot be predicted until the time of encoding.

An <b>IWMCodecInfo</b> interface exists for each profile manager object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the profile manager object, typically <b>IWMProfileManager</b>.

The methods of the <b>IWMCodecInfo</b> interface are inherited by <b>IWMCodecInfo2</b> and <b>IWMCodecInfo3</b>.

## -inheritance

The <b>IWMCodecInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2">IWMCodecInfo2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3">IWMCodecInfo3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>
