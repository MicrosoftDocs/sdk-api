---
UID: NN:mfidl.IMFByteStreamCacheControl
title: IMFByteStreamCacheControl
author: windows-driver-content
description: Controls how a network byte stream transfers data to a local cache.
old-location: mf\imfbytestreamcachecontrol.htm
old-project: medfound
ms.assetid: e12a532a-4624-4e06-8e19-6e9daec550ac
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFByteStreamCacheControl, IMFByteStreamCacheControl interface [Media Foundation], IMFByteStreamCacheControl interface [Media Foundation],described, mf.imfbytestreamcachecontrol, mfidl/IMFByteStreamCacheControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFByteStreamCacheControl
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamCacheControl interface


## -description


Controls how a network byte stream transfers data to a local cache. Optionally, this interface is exposed by byte streams that read data from a network, for example, through HTTP.
      

To get a pointer to this interface, call <b>QueryInterface</b> on the byte stream object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamCacheControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFByteStreamCacheControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamCacheControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f0f7102-c839-4e92-a798-5ea31ceba013">StopBackgroundTransfer</a>
</td>
<td align="left" width="63%">
Stops the background transfer of data to the local cache.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>



<a href="https://msdn.microsoft.com/bbf9cdb1-5ec7-498a-aa59-85c24779547e">IMFByteStreamBuffering</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

