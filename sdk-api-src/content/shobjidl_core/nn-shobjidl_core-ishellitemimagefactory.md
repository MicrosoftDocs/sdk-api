---
UID: NN:shobjidl_core.IShellItemImageFactory
title: IShellItemImageFactory (shobjidl_core.h)
author: windows-sdk-content
description: Exposes a method to return either icons or thumbnails for Shell items. If no thumbnail or icon is available for the requested item, a per-class icon may be provided from the Shell.
old-location: shell\IShellItemImageFactory.htm
tech.root: shell
ms.assetid: a6eea412-553a-4bdd-afc2-cc002c4500a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellItemImageFactory, IShellItemImageFactory interface [Windows Shell], IShellItemImageFactory interface [Windows Shell],described, _shell_IShellItemImageFactory, shell.IShellItemImageFactory, shobjidl_core/IShellItemImageFactory
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IShellItemImageFactory"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IShellItemImageFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellItemImageFactory interface


## -description


Exposes a method to return either icons or thumbnails for Shell items. If no thumbnail or icon is available for the requested item, a per-class icon may be provided from the Shell.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItemImageFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellItemImageFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItemImageFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemimagefactory-getimage">GetImage</a>
</td>
<td align="left" width="63%">
Gets an HBITMAP that represents an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>. The default behavior is to load a thumbnail. If there is no thumbnail for the current <b>IShellItem</b>, it retrieves an HBITMAP for the icon of the item. The thumbnail or icon is extracted if it is not currently cached.

</td>
</tr>
</table> 


## -remarks



A pointer to this interface is commonly obtained through one of the following functions:
                
                

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist">SHCreateItemFromIDList</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname">SHCreateItemFromParsingName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename">SHCreateItemFromRelativeName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder">SHCreateItemInKnownFolder</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent">SHCreateItemWithParent</a>
</li>
</ul>
See the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940383(v=vs.85)">Using Image Factory</a> sample for a full example of how to use this interface.



