---
UID: NN:wmsdkidl.IWMSyncReader2
title: IWMSyncReader2
author: windows-driver-content
description: The IWMSyncReader2 interface provides advanced features for the synchronous reader.
old-location: wmformat\iwmsyncreader2.htm
old-project: wmformat
ms.assetid: f3db7530-a662-46f1-bc64-1dd4523dc87c
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMSyncReader2, IWMSyncReader2 interface [windows Media Format], IWMSyncReader2 interface [windows Media Format], described, IWMSyncReader2Interface, wmformat.iwmsyncreader2, wmsdkidl/IWMSyncReader2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMSyncReader2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader2 interface


## -description



The <b>IWMSyncReader2</b> interface provides advanced features for the synchronous reader. It contains methods for allocating samples manually and for seeking to SMPTE time codes.

An <b>IWMSyncReader2</b> interface exists for every synchronous reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the synchronous reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSyncReader2</b> interface inherits from <a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader</a>. <b>IWMSyncReader2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSyncReader2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aef68130-57a8-4bb6-8091-8ee2c75bdf76">GetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IWMReaderAllocatorEx</b> interface for allocating output samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88f02e2d-2585-4668-869b-d42739c02a5c">GetAllocateForStream</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IWMReaderAllocatorEx</b> interface for allocating stream samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f0c754e-f09c-472f-8f40-3fcd0fb29c48">SetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Sets an <b>IWMReaderAllocatorEx</b> interface for allocating output samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed94977e-e930-4045-a69d-36109e7e21c9">SetAllocateForStream</a>
</td>
<td align="left" width="63%">
Sets an <b>IWMReaderAllocatorEx</b> interface for allocating stream samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a21529f-3645-4fe5-900e-19032d601ff4">SetRangeByFrameEx</a>
</td>
<td align="left" width="63%">
Enables you to play a portion of a file specified by frame numbers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/304564b1-6ae3-4e1c-bea9-7a49c522a914">SetRangeByTimecode</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback using SMPTE time codes.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by calling the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

