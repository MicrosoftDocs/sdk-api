---
UID: NN:wmsdkidl.IWMImageInfo
title: IWMImageInfo
author: windows-sdk-content
description: The IWMImageInfo interface retrieves images stored in ID3v2 &#0034;APIC&#0034; (attached picture) frames in a file.
old-location: wmformat\iwmimageinfo.htm
old-project: wmformat
ms.assetid: 1b3b4224-f86d-437c-969e-fe30e6d002a8
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMImageInfo, IWMImageInfo interface [windows Media Format], IWMImageInfo interface [windows Media Format],described, IWMImageInfoInterface, wmformat.iwmimageinfo, wmsdkidl/IWMImageInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WM_AETYPE
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMImageInfo interface


## -description



The <b>IWMImageInfo</b> interface retrieves images stored in ID3v2 "APIC" (attached picture) frames in a file. The methods of this interface are superseded in the Windows Media Format 9 Series SDK by the <a href="https://msdn.microsoft.com/ec82dfdf-7755-4758-9771-096aac114f78">WM/Picture</a> metadata attribute, which is supported by the methods of the new <a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a> interface. If you are using the Windows Media Format 9 Series SDK, you should avoid using this interface.

An <b>IWMImageInfo</b> interface exists for every reader, synchronous reader, and metadata editor object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface in one of these objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMImageInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMImageInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fe1dcd53-fcdd-4190-9a07-65d0b34112d0">GetImage</a>
</td>
<td align="left" width="63%">
Retrieves an image stored in a file as an ID3v2 "APIC" metadata frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95cf5906-9cbc-4bba-8892-236672cf4068">GetImageCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of images stored in a file using ID3v2 "APIC" frames.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



If retrieving this interface from the metadata editor, you must wait until after the file has been opened to call <b>QueryInterface</b>. If you try to <b>QueryInterface</b> for <b>IWMImageInfo</b> before receiving the WMT_OPENED message in your <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method, the call will fail.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>
 

 

