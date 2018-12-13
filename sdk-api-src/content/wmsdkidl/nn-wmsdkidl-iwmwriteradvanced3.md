---
UID: NN:wmsdkidl.IWMWriterAdvanced3
title: IWMWriterAdvanced3
author: windows-sdk-content
description: The IWMWriterAdvanced3 interface provides additional functionality for the writer object.IWMWriterAdvanced3 exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
old-location: wmformat\iwmwriteradvanced3.htm
tech.root: wmformat
ms.assetid: 99f7e4f7-0080-498d-b4f1-960c4955b4db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterAdvanced3, IWMWriterAdvanced3 interface [windows Media Format], IWMWriterAdvanced3 interface [windows Media Format],described, IWMWriterAdvanced3Interface, wmformat.iwmwriteradvanced3, wmsdkidl/IWMWriterAdvanced3
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
 - IWMWriterAdvanced3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterAdvanced3 interface


## -description



The <b>IWMWriterAdvanced3</b> interface provides additional functionality for the writer object.

<b>IWMWriterAdvanced3</b> exists for every instance of the writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterAdvanced3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd798721(v=VS.85).aspx">IWMWriterAdvanced2</a>. <b>IWMWriterAdvanced3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterAdvanced3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798725(v=VS.85).aspx">GetStatisticsEx</a>
</td>
<td align="left" width="63%">
Retrieves extended statistics for the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798726(v=VS.85).aspx">SetNonBlocking</a>
</td>
<td align="left" width="63%">
Configures the writer so that it does not block the calling thread.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798720(v=VS.85).aspx">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798721(v=VS.85).aspx">IWMWriterAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>



<a href="https://msdn.microsoft.com/d722b676-bf65-4f91-8118-bb12d3bbb6cb">Writing ASF Files</a>
 

 

