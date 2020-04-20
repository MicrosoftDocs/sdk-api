---
UID: NN:wmp.IWMPLibraryServices
title: IWMPLibraryServices (wmp.h)
description: The IWMPLibraryServices interface provides methods to enumerate libraries.helpviewer_keywords: ["IWMPLibraryServices","IWMPLibraryServices interface [Windows Media Player]","IWMPLibraryServices interface [Windows Media Player]","described","IWMPLibraryServicesInterface","wmp.iwmplibraryservices","wmp/IWMPLibraryServices"]
old-location: wmp\iwmplibraryservices.htm
tech.root: WMP
ms.assetid: 9ed6d02e-15ca-425f-8642-e32a5adfaa55
ms.date: 12/05/2018
ms.keywords: IWMPLibraryServices, IWMPLibraryServices interface [Windows Media Player], IWMPLibraryServices interface [Windows Media Player],described, IWMPLibraryServicesInterface, wmp.iwmplibraryservices, wmp/IWMPLibraryServices
f1_keywords:
- wmp/IWMPLibraryServices
dev_langs:
- c++
req.header: wmp.h
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
- wmp.h
api_name:
- IWMPLibraryServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPLibraryServices interface


## -description



The <b>IWMPLibraryServices</b> interface provides methods to enumerate libraries.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPLibraryServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPLibraryServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPLibraryServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype">getCountByType</a>
</td>
<td align="left" width="63%">
Retrieves the count of available libraries of a specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype">getLibraryByType</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPLibrary</b> interface that represents the library that has the specified type and index.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPLibraryServices</b> by calling <b>QueryInterface</b> through <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer</a> from a local or remoted Windows Media Player ActiveX control.
	
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

