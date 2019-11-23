---
UID: NN:wmp.IWMPCdromBurn
title: IWMPCdromBurn (wmp.h)

description: The IWMPCdromBurn interface provides methods to manage creating audio CDs.
old-location: wmp\iwmpcdromburn.htm
tech.root: WMP
ms.assetid: 45116a33-62f9-4c7d-b246-25905cbaf118

ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn, IWMPCdromBurn interface [Windows Media Player], IWMPCdromBurn interface [Windows Media Player],described, IWMPCdromBurnInterface, wmp.iwmpcdromburn, wmp/IWMPCdromBurn
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPCdromBurn"
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
 - IWMPCdromBurn
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCdromBurn interface


## -description



The <b>IWMPCdromBurn</b> interface provides methods to manage creating audio CDs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCdromBurn</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPCdromBurn</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPCdromBurn</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase">erase</a>
</td>
<td align="left" width="63%">
Erases the current CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnformat">get_burnFormat</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the type of CD to burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnplaylist">get_burnPlaylist</a>
</td>
<td align="left" width="63%">
Retrieves the current playlist to burn to the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress">get_burnProgress</a>
</td>
<td align="left" width="63%">
Retrieves the CD burning progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate">get_burnState</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration value that indicates the current burn state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_label">get_label</a>
</td>
<td align="left" width="63%">
Retrieves the CD volume label string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified attribute for the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable">isAvailable</a>
</td>
<td align="left" width="63%">
Provides information about the CD drive and media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat">put_burnFormat</a>
</td>
<td align="left" width="63%">
Specifies the type of CD to burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist">put_burnPlaylist</a>
</td>
<td align="left" width="63%">
Specifies the playlist to burn to CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label">put_label</a>
</td>
<td align="left" width="63%">
Specifies the label string for the CD volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus">refreshStatus</a>
</td>
<td align="left" width="63%">
Updates the status information for the current burn playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn">startBurn</a>
</td>
<td align="left" width="63%">
Burns the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn">stopBurn</a>
</td>
<td align="left" width="63%">
Stops the CD burning process.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

