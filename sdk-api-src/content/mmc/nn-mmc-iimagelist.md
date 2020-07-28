---
UID: NN:mmc.IImageList
title: IImageList (mmc.h)
description: The IImageList interface enables the user to insert images to be used as icons for items in the result or scope pane of the console.
helpviewer_keywords: ["IImageList","IImageList interface [MMC]","IImageList interface [MMC]","described","_slate_iimagelist","mmc.iimagelist","mmc/IImageList"]
old-location: mmc\iimagelist.htm
tech.root: mmc
ms.assetid: a957239b-6cb2-4101-adeb-e9ba4f876af4
ms.date: 12/05/2018
ms.keywords: IImageList, IImageList interface [MMC], IImageList interface [MMC],described, _slate_iimagelist, mmc.iimagelist, mmc/IImageList
f1_keywords:
- mmc/IImageList
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmcndmgr.dll
api_name:
- IImageList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IImageList interface


## -description


The 
<b>IImageList</b> interface enables the user to insert images to be used as icons for items in the result or scope pane of the console. When an image is inserted, an index is passed in and associated with the image. Any time the image is to be used, the user can refer to it by the index that he or she assigned.

Be aware that because the image list is shared among many components, the user-specified index is a "virtual" index that gets mapped internally to the actual index.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImageList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImageList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImageList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iimagelist-imagelistseticon">ImageListSetIcon</a>
</td>
<td align="left" width="63%">
Sets an icon in the image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iimagelist-imagelistsetstrip">ImageListSetStrip</a>
</td>
<td align="left" width="63%">
Sets a strip of icons in the image list.

</td>
</tr>
</table> 

