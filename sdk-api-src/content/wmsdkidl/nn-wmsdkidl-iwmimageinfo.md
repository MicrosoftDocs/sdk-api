---
UID: NN:wmsdkidl.IWMImageInfo
title: IWMImageInfo (wmsdkidl.h)
author: windows-sdk-content
description: The IWMImageInfo interface retrieves images stored in ID3v2 &#0034;APIC&#0034; (attached picture) frames in a file.
old-location: wmformat\iwmimageinfo.htm
tech.root: wmformat
ms.assetid: 1b3b4224-f86d-437c-969e-fe30e6d002a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMImageInfo, IWMImageInfo interface [windows Media Format], IWMImageInfo interface [windows Media Format],described, IWMImageInfoInterface, wmformat.iwmimageinfo, wmsdkidl/IWMImageInfo
ms.topic: interface
f1_keywords: ["wmsdkidl/IWMImageInfo"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMImageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMImageInfo interface


## -description



The <b>IWMImageInfo</b> interface retrieves images stored in ID3v2 "APIC" (attached picture) frames in a file. The methods of this interface are superseded in the Windows Media Format 9 Series SDK by the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmpicture">WM/Picture</a> metadata attribute, which is supported by the methods of the new <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a> interface. If you are using the Windows Media Format 9 Series SDK, you should avoid using this interface.

An <b>IWMImageInfo</b> interface exists for every reader, synchronous reader, and metadata editor object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface in one of these objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMImageInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMImageInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMImageInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmimageinfo-getimage">GetImage</a>
</td>
<td align="left" width="63%">
Retrieves an image stored in a file as an ID3v2 "APIC" metadata frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmimageinfo-getimagecount">GetImageCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of images stored in a file using ID3v2 "APIC" frames.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



If retrieving this interface from the metadata editor, you must wait until after the file has been opened to call <b>QueryInterface</b>. If you try to <b>QueryInterface</b> for <b>IWMImageInfo</b> before receiving the WMT_OPENED message in your <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method, the call will fail.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>
 

 

