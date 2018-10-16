---
UID: NN:mfidl.IMFSeekInfo
title: IMFSeekInfo
author: windows-sdk-content
description: For a particular seek position, gets the two nearest key frames.
old-location: mf\imfseekinfo.htm
tech.root: medfound
ms.assetid: 5B1AD3A1-D5ED-4F9D-A895-0312E6EB3072
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFSeekInfo, IMFSeekInfo interface [Media Foundation], IMFSeekInfo interface [Media Foundation],described, mf.imfseekinfo, mfidl/IMFSeekInfo
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSeekInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSeekInfo interface


## -description


For a particular seek position, gets the two nearest key frames.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSeekInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSeekInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSeekInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72A7161A-09CA-4582-B240-1442D70936D7">GetNearestKeyFrames</a>
</td>
<td align="left" width="63%">
For a particular seek position, gets the two nearest key frames.

</td>
</tr>
</table> 


## -remarks



A media source can implement this interface as an optional service. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/119e9e2f-0e26-4dfc-9c89-156b63a63640">IMFGetService::GetService</a> with the service identifier <b>MF_SCRUBBING_SERVICE</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

