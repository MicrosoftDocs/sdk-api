---
UID: NN:wmpservices.IWMPServices
title: IWMPServices
author: windows-sdk-content
description: The IWMPServices interface is implemented by Windows Media Player. It provides methods to retrieve the current stream state and current stream time.
old-location: wmp\iwmpservices.htm
tech.root: WMP
ms.assetid: 26d68b4b-4eeb-42e2-a1d1-0d0e73725059
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPServices, IWMPServices interface [Windows Media Player], IWMPServices interface [Windows Media Player],described, IWMPServicesInterfaceDSP, wmp.iwmpservices, wmpservices/IWMPServices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPServices interface


## -description



The <b>IWMPServices</b> interface is implemented by Windows Media Player. It provides methods to retrieve the current stream state and current stream time.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a73ea54-45ce-47ff-b551-10aab2798420">GetStreamState</a>
</td>
<td align="left" width="63%">
Returns a value that represents the current stream state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e6c8181-3ff9-4ce1-aad5-9d7821771f69">GetStreamTime</a>
</td>
<td align="left" width="63%">
Returns a value that indicates the current stream time.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4660f928-2e92-468f-9e2b-b411931dfded">DSP Plug-in Interfaces</a>
 

 

