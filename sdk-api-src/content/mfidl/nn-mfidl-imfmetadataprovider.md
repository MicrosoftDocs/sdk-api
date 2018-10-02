---
UID: NN:mfidl.IMFMetadataProvider
title: IMFMetadataProvider
author: windows-sdk-content
description: Gets metadata from a media source or other object.
old-location: mf\imfmetadataprovider.htm
tech.root: MedFound
ms.assetid: f32e78c9-a567-448d-947d-d7ea996bba5e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFMetadataProvider, IMFMetadataProvider interface [Media Foundation], IMFMetadataProvider interface [Media Foundation],described, f32e78c9-a567-448d-947d-d7ea996bba5e, mf.imfmetadataprovider, mfidl/IMFMetadataProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMetadataProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMetadataProvider interface


## -description


Gets metadata from a media source or other object.

If a media source supports this interface, it must expose the interface as a service. To get a pointer to this interface from a media source, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. The service identifier is <b>MF_METADATA_PROVIDER_SERVICE</b>. Other types of object can expose this interface through <b>QueryInterface</b>.

Use this interface to get a pointer to the <a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMetadataProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMetadataProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMetadataProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a3c1932-c301-4ecd-b640-02d7bcfc2aca">GetMFMetadata</a>
</td>
<td align="left" width="63%">
Gets a collection of metadata, either for an entire presentation, or for one stream in the presentation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>



<a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>
 

 

