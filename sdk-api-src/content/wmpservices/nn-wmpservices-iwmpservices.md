---
UID: NN:wmpservices.IWMPServices
title: IWMPServices (wmpservices.h)
author: windows-sdk-content
description: The IWMPServices interface is implemented by Windows Media Player. It provides methods to retrieve the current stream state and current stream time.
old-location: wmp\iwmpservices.htm
tech.root: WMP
ms.assetid: 26d68b4b-4eeb-42e2-a1d1-0d0e73725059
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPServices, IWMPServices interface [Windows Media Player], IWMPServices interface [Windows Media Player],described, IWMPServicesInterfaceDSP, wmp.iwmpservices, wmpservices/IWMPServices
ms.topic: interface
f1_keywords: 
 - "wmpservices/IWMPServices"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPServices interface


## -description



The <b>IWMPServices</b> interface is implemented by Windows Media Player. It provides methods to retrieve the current stream state and current stream time.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPServices</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmpservices-getstreamstate">GetStreamState</a>
</td>
<td align="left" width="63%">
Returns a value that represents the current stream state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmpservices-getstreamtime">GetStreamTime</a>
</td>
<td align="left" width="63%">
Returns a value that indicates the current stream time.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/dsp-plug-in-interfaces">DSP Plug-in Interfaces</a>
 

 

