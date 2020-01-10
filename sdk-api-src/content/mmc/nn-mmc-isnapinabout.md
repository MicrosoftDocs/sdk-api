---
UID: NN:mmc.ISnapinAbout
title: ISnapinAbout (mmc.h)
description: The ISnapinAbout interface enables the console to get copyright and version information from a snap-in. The console also uses this interface to obtain images for the static folder from the snap-in.
old-location: mmc\isnapinabout.htm
tech.root: mmc
ms.assetid: 39732334-f849-433b-a313-0c4a675bf408
ms.date: 12/05/2018
ms.keywords: ISnapinAbout, ISnapinAbout interface [MMC], ISnapinAbout interface [MMC],described, _slate_isnapinabout, mmc.isnapinabout, mmc/ISnapinAbout
f1_keywords:
- mmc/ISnapinAbout
dev_langs:
- c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
- Mmc.h
api_name:
- ISnapinAbout
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISnapinAbout interface


## -description


The 
<b>ISnapinAbout</b> interface enables the console to get copyright and version information from a snap-in. The console also uses this interface to obtain images for the static folder from the snap-in.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinAbout</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISnapinAbout</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISnapinAbout</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-isnapinabout-getprovider">GetProvider</a>
</td>
<td align="left" width="63%">
Obtains the name of the snap-in provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-isnapinabout-getsnapindescription">GetSnapinDescription</a>
</td>
<td align="left" width="63%">
Obtains snap-in description box text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-isnapinabout-getsnapinimage">GetSnapinImage</a>
</td>
<td align="left" width="63%">
Obtains the main icon for the <b>About</b> box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-isnapinabout-getsnapinversion">GetSnapinVersion</a>
</td>
<td align="left" width="63%">
Obtains the version number of the snap-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-isnapinabout-getstaticfolderimage">GetStaticFolderImage</a>
</td>
<td align="left" width="63%">
Obtains static folder images for both the scope and result panes.

</td>
</tr>
</table> 

