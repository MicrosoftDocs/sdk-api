---
UID: NN:wmpservices.IWMPConvert
title: IWMPConvert
author: windows-driver-content
description: The IWMPConvert interface provides methods to enable Windows Media Player conversion plug-ins to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).
old-location: wmp\iwmpconvert.htm
old-project: WMP
ms.assetid: 316d1a13-0803-4414-8c51-0d5c4768b06d
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPConvert, IWMPConvert interface [Windows Media Player], IWMPConvert interface [Windows Media Player], described, IWMPConvertInterface, wmp.iwmpconvert, wmpservices/IWMPConvert
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmpservices.h
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
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmpservices.h
api_name:
-	IWMPConvert
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPConvert interface


## -description



The <b>IWMPConvert</b> interface provides methods to enable Windows Media Player conversion plug-ins to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPConvert</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPConvert</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPConvert</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69ca3863-94ec-457f-9f93-aebb5b80c8a9">ConvertFile</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to enable a conversion plug-in to convert a digital media file into ASF.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27a2ff9a-0c95-4c82-8e4a-c91d2a595005">GetErrorURL</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve the URL of a webpage that displays error information about a file conversion.

</td>
</tr>
</table> 


## -remarks




These methods are implemented by a conversion plug-in and called by Windows Media Player. 
	 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

