---
UID: NN:wmpservices.IWMPConvert
title: IWMPConvert (wmpservices.h)
description: The IWMPConvert interface provides methods to enable Windows Media Player conversion plug-ins to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).helpviewer_keywords: ["IWMPConvert","IWMPConvert interface [Windows Media Player]","IWMPConvert interface [Windows Media Player]","described","IWMPConvertInterface","wmp.iwmpconvert","wmpservices/IWMPConvert"]
old-location: wmp\iwmpconvert.htm
tech.root: WMP
ms.assetid: 316d1a13-0803-4414-8c51-0d5c4768b06d
ms.date: 12/05/2018
ms.keywords: IWMPConvert, IWMPConvert interface [Windows Media Player], IWMPConvert interface [Windows Media Player],described, IWMPConvertInterface, wmp.iwmpconvert, wmpservices/IWMPConvert
f1_keywords:
- wmpservices/IWMPConvert
dev_langs:
- c++
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
- IWMPConvert
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPConvert interface


## -description



The <b>IWMPConvert</b> interface provides methods to enable Windows Media Player conversion plug-ins to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPConvert</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPConvert</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile">ConvertFile</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to enable a conversion plug-in to convert a digital media file into ASF.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-geterrorurl">GetErrorURL</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve the URL of a webpage that displays error information about a file conversion.

</td>
</tr>
</table> 


## -remarks



These methods are implemented by a conversion plug-in and called by Windows Media Player. 
	 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

