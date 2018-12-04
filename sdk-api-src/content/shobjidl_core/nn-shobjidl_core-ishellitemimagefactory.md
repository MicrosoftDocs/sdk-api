---
UID: NN:shobjidl_core.IShellItemImageFactory
title: IShellItemImageFactory
author: windows-sdk-content
description: Exposes a method to return either icons or thumbnails for Shell items. If no thumbnail or icon is available for the requested item, a per-class icon may be provided from the Shell.
old-location: shell\IShellItemImageFactory.htm
tech.root: shell
ms.assetid: a6eea412-553a-4bdd-afc2-cc002c4500a4
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IShellItemImageFactory, IShellItemImageFactory interface [Windows Shell], IShellItemImageFactory interface [Windows Shell],described, _shell_IShellItemImageFactory, shell.IShellItemImageFactory, shobjidl_core/IShellItemImageFactory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItemImageFactory interface


## -description


Exposes a method to return either icons or thumbnails for Shell items. If no thumbnail or icon is available for the requested item, a per-class icon may be provided from the Shell.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItemImageFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellItemImageFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b31a5eb7-f12f-41e0-9047-450240371424">GetImage</a>
</td>
<td align="left" width="63%">
Gets an HBITMAP that represents an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>. The default behavior is to load a thumbnail. If there is no thumbnail for the current <b>IShellItem</b>, it retrieves an HBITMAP for the icon of the item. The thumbnail or icon is extracted if it is not currently cached.

</td>
</tr>
</table> 


## -remarks



A pointer to this interface is commonly obtained through one of the following functions:
                
                

<ul>
<li>
<a href="https://msdn.microsoft.com/a6dcddd9-cdbc-4cf9-97e3-d1b562283344">SHCreateItemFromIDList</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81e48318-b6a4-4b1a-8b78-21c00b9dc485">SHCreateItemFromParsingName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/af6c2e8b-c812-4858-a9db-24549dedc2aa">SHCreateItemFromRelativeName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dc75ee60-7319-4a11-949e-dd0c3deabd8f">SHCreateItemInKnownFolder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8fb84a20-d8f2-4c7c-bfb1-a22791b8636a">SHCreateItemWithParent</a>
</li>
</ul>
See the <a href="https://msdn.microsoft.com/63B1D242-A52A-4796-90D7-A5AC8E3002B4">Using Image Factory</a> sample for a full example of how to use this interface.



