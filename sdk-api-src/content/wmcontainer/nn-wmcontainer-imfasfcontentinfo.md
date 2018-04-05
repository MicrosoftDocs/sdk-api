---
UID: NN:wmcontainer.IMFASFContentInfo
title: IMFASFContentInfo
author: windows-driver-content
description: Provides methods to work with the header section of files conforming to the Advanced Systems Format (ASF) specification.
old-location: mf\imfasfcontentinfo.htm
old-project: medfound
ms.assetid: 9f490e6a-f378-45c1-a69d-985c6e884358
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 9f490e6a-f378-45c1-a69d-985c6e884358, IMFASFContentInfo, IMFASFContentInfo interface [Media Foundation], IMFASFContentInfo interface [Media Foundation], described, mf.imfasfcontentinfo, wmcontainer/IMFASFContentInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFContentInfo
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFContentInfo interface


## -description



          Provides methods to work with the header section of files conforming to the Advanced Systems Format (ASF) specification. 

The <a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a> exposes this interface. To create the get a pointer to the <b>IMFASFContentInfo</b> interface, call <a href="https://msdn.microsoft.com/00460f79-7033-4893-88c0-b1c939441f70">MFCreateASFContentInfo</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFContentInfo</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFASFContentInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFContentInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e">GenerateHeader</a>
</td>
<td align="left" width="63%">
Encodes the data in the ASF ContentInfo object into a binary ASF header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f22cb48d-1346-4182-8ca2-f57a7fdc76e4">GeneratePresentationDescriptor</a>
</td>
<td align="left" width="63%">
Creates a presentation descriptor for the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e77a5564-82bc-4c1d-9fb8-84ab484c4ca8">GetEncodingConfigurationPropertyStore</a>
</td>
<td align="left" width="63%">
Retrieves a property store that can be used to set encoding properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c13ee7e6-df59-448f-80c4-04ac7c8c98ed">GetHeaderSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the header section of an ASF file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f74c896-a0c0-407b-b893-de15863bc2eb">GetProfile</a>
</td>
<td align="left" width="63%">
Retrieves an ASF profile that describes the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/149e2514-74e5-403b-925f-53a17dbbcb64">ParseHeader</a>
</td>
<td align="left" width="63%">
Parses the information in an ASF header and uses that information to set values in the ContentInfo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e7e062d-9507-400a-8cc2-5355c12017f5">SetProfile</a>
</td>
<td align="left" width="63%">
Uses profile data from a profile object to configure settings in the ContentInfo object

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

