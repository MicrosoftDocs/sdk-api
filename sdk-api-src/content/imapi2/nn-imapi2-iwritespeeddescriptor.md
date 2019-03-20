---
UID: NN:imapi2.IWriteSpeedDescriptor
title: IWriteSpeedDescriptor (imapi2.h)
author: windows-sdk-content
description: Use this interface retrieve detailed write configurations supported by the disc recorder and current media, for example, the media type, write speed, rotational-speed control type.
old-location: imapi\iwritespeeddescriptor.htm
tech.root: imapi
ms.assetid: 9efaa744-ae0c-4101-8d78-091cba990533
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWriteSpeedDescriptor, IWriteSpeedDescriptor interface [IMAPI], IWriteSpeedDescriptor interface [IMAPI],described, imapi.iwritespeeddescriptor, imapi2/IWriteSpeedDescriptor
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IWriteSpeedDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWriteSpeedDescriptor interface


## -description


Use this interface retrieve detailed write configurations supported by the disc recorder and current media, for example, the media type, write speed, rotational-speed control type.

To get this interface, call one of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/9eb84ec6-900a-45ba-9111-9c9c6b3f5bb2">IDiscFormat2Data::get_SupportedWriteSpeedDescriptors</a>
</li>
<li>
<a href="https://msdn.microsoft.com/00a7c10a-7790-4193-928c-d3211047dbbe">IDiscFormat2RawCD::get_SupportedWriteSpeedDescriptors</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a0aefc38-c679-4492-becc-a8c8563ea948">IDiscFormat2TrackAtOnce::get_SupportedWriteSpeedDescriptors</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWriteSpeedDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWriteSpeedDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWriteSpeedDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4608fb27-8d8c-4ccc-9838-bdbe9dadee83">get_MediaType</a>
</td>
<td align="left" width="63%">
Retrieves type of media in the current drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36c509a2-6592-4fa0-8e4a-4b21f4cf7a13">get_RotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the supported rotational-speed control used by the recorder for the current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9136a735-d902-48bc-bddd-297c1e32310e">get_WriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the supported write speed for writing to the media.

</td>
</tr>
</table> 


## -remarks



This is a <b>MsftWriteSpeedDescriptor</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/9eb84ec6-900a-45ba-9111-9c9c6b3f5bb2">IDiscFormat2Data::get_SupportedWriteSpeedDescriptors</a>



<a href="https://msdn.microsoft.com/00a7c10a-7790-4193-928c-d3211047dbbe">IDiscFormat2RawCD::get_SupportedWriteSpeedDescriptors</a>



<a href="https://msdn.microsoft.com/a0aefc38-c679-4492-becc-a8c8563ea948">IDiscFormat2TrackAtOnce::get_SupportedWriteSpeedDescriptors</a>
 

 

