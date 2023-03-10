---
UID: NN:wmsdkidl.IWMImageInfo
title: IWMImageInfo (wmsdkidl.h)
description: The IWMImageInfo interface retrieves images stored in ID3v2 &#0034;APIC&#0034; (attached picture) frames in a file.
helpviewer_keywords: ["IWMImageInfo","IWMImageInfo interface [windows Media Format]","IWMImageInfo interface [windows Media Format]","described","IWMImageInfoInterface","wmformat.iwmimageinfo","wmsdkidl/IWMImageInfo"]
old-location: wmformat\iwmimageinfo.htm
tech.root: wmformat
ms.assetid: 1b3b4224-f86d-437c-969e-fe30e6d002a8
ms.date: 12/05/2018
ms.keywords: IWMImageInfo, IWMImageInfo interface [windows Media Format], IWMImageInfo interface [windows Media Format],described, IWMImageInfoInterface, wmformat.iwmimageinfo, wmsdkidl/IWMImageInfo
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
 - IWMImageInfo
 - wmsdkidl/IWMImageInfo
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
 - IWMImageInfo
---

# IWMImageInfo interface


## -description

The <b>IWMImageInfo</b> interface retrieves images stored in ID3v2 "APIC" (attached picture) frames in a file. The methods of this interface are superseded in the Windows Media Format 9 Series SDK by the <a href="/windows/desktop/wmformat/wmpicture">WM/Picture</a> metadata attribute, which is supported by the methods of the new <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a> interface. If you are using the Windows Media Format 9 Series SDK, you should avoid using this interface.

An <b>IWMImageInfo</b> interface exists for every reader, synchronous reader, and metadata editor object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface in one of these objects.

## -inheritance

The <b>IWMImageInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMImageInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

If retrieving this interface from the metadata editor, you must wait until after the file has been opened to call <b>QueryInterface</b>. If you try to <b>QueryInterface</b> for <b>IWMImageInfo</b> before receiving the WMT_OPENED message in your <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method, the call will fail.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>
