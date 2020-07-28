---
UID: NN:wmp.IWMPRemoteMediaServices
title: IWMPRemoteMediaServices (wmp.h)
description: The IWMPRemoteMediaServices interface includes methods that provide services to Windows Media Player from a program that hosts the Player control. These methods are designed to be used with C++, and some methods can only be used with remoting.
helpviewer_keywords: ["IWMPRemoteMediaServices","IWMPRemoteMediaServices interface [Windows Media Player]","IWMPRemoteMediaServices interface [Windows Media Player]","described","IWMPRemoteMediaServicesInterface","wmp.iwmpremotemediaservices","wmp/IWMPRemoteMediaServices"]
old-location: wmp\iwmpremotemediaservices.htm
tech.root: WMP
ms.assetid: 594a614a-8da1-4ef0-a6af-01284fb48ef7
ms.date: 12/05/2018
ms.keywords: IWMPRemoteMediaServices, IWMPRemoteMediaServices interface [Windows Media Player], IWMPRemoteMediaServices interface [Windows Media Player],described, IWMPRemoteMediaServicesInterface, wmp.iwmpremotemediaservices, wmp/IWMPRemoteMediaServices
f1_keywords:
- wmp/IWMPRemoteMediaServices
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
- IWMPRemoteMediaServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPRemoteMediaServices interface


## -description



The <b>IWMPRemoteMediaServices</b> interface includes methods that provide services to Windows Media Player from a program that hosts the Player control. These methods are designed to be used with C++, and some methods can only be used with remoting.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPRemoteMediaServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPRemoteMediaServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPRemoteMediaServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname">GetApplicationName</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve the name of the program that is hosting the remoted control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode">GetCustomUIMode</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve the location of a skin file to apply to the Player control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getscriptableobject">GetScriptableObject</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve a name and interface pointer for an object that can be called from the script code within a skin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype">GetServiceType</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to determine whether a host program wants to run its embedded control remotely.

</td>
</tr>
</table> 

A pointer to an <b>IWMPRemoteMediaServices</b> interface is retrieved by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
 

 

