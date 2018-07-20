---
UID: NN:mfidl.IMFByteStreamTimeSeek
title: IMFByteStreamTimeSeek
author: windows-sdk-content
description: Seeks a byte stream by time position.
old-location: mf\imfbytestreamtimeseek.htm
old-project: medfound
ms.assetid: BD9EDFF7-46BA-4788-A44E-C69C4B0BEB50
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFByteStreamTimeSeek, IMFByteStreamTimeSeek interface [Media Foundation], IMFByteStreamTimeSeek interface [Media Foundation],described, mf.imfbytestreamtimeseek, mfidl/IMFByteStreamTimeSeek
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamTimeSeek
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamTimeSeek interface


## -description


Seeks a byte stream by time position.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamTimeSeek</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFByteStreamTimeSeek</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamTimeSeek</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D56E1F06-AA05-430C-BF5C-30B38831B842">GetTimeSeekResult</a>
</td>
<td align="left" width="63%">
Gets the result of a time-based seek.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92FCE0EF-046C-4639-958E-731795C5A123">IsTimeSeekSupported</a>
</td>
<td align="left" width="63%">
Queries whether the byte stream supports time-based seeking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/786F1299-A9E2-4B2C-A6AE-F88E6BF022DC">TimeSeek</a>
</td>
<td align="left" width="63%">
Seeks to a new position in the byte stream.

</td>
</tr>
</table> 


## -remarks



A byte stream can implement this interface if it supports time-based seeking. For example, a byte stream that reads data from a server  might implement the interface. Typically, a local file-based byte stream would not implement it.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the byte stream object.




## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

