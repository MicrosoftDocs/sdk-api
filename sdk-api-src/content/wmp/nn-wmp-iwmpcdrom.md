---
UID: NN:wmp.IWMPCdrom
title: IWMPCdrom (wmp.h)

description: The IWMPCdrom interface provides a way to access a CD or DVD in its drive.
old-location: wmp\iwmpcdrom.htm
tech.root: WMP
ms.assetid: 323a6841-ffbd-4bbb-ac04-1d121cf5bd06

ms.date: 12/05/2018
ms.keywords: IWMPCdrom, IWMPCdrom interface [Windows Media Player], IWMPCdrom interface [Windows Media Player],described, IWMPCdromInterface, wmp.iwmpcdrom, wmp/IWMPCdrom
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPCdrom"
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
 - IWMPCdrom
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCdrom interface


## -description



The <b>IWMPCdrom</b> interface provides a way to access a CD or DVD in its drive.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCdrom</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPCdrom</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPCdrom</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-eject">eject</a>
</td>
<td align="left" width="63%">
Ejects the CD or DVD from the drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_drivespecifier">get_driveSpecifier</a>
</td>
<td align="left" width="63%">
Retrieves the CD or DVD drive letter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist">get_playlist</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface representing the tracks on a CD or the root-level title entries for a DVD.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPCdrom</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection">IWMPCdromCollection</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item">item</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

