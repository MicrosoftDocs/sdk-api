---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IShellItemImageFactory::GetImage


## -description


Gets an <b>HBITMAP</b> that represents an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>. The default behavior is to load a thumbnail. If there is no thumbnail for the current <b>IShellItem</b>, it retrieves an <b>HBITMAP</b> for the icon of the item. The thumbnail or icon is extracted if it is not currently cached.


## -parameters




### -param size [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a></b>

A structure that specifies the size of the image to be received.


### -param flags [in]

Type: <b>SIIGBF</b>

One or more of the following:



#### SIIGBF_RESIZETOFIT (0x00000000)

Shrink the bitmap as necessary to fit, preserving its aspect ratio.



#### SIIGBF_BIGGERSIZEOK (0x00000001)

Passed by callers if they want to stretch the returned image themselves. For example, if the caller passes an icon size of 80x80, a 96x96 thumbnail could be returned. This action can be used as a performance optimization if the caller expects that they will need to stretch the image. Note that the Shell implementation of <a href="https://msdn.microsoft.com/a6eea412-553a-4bdd-afc2-cc002c4500a4">IShellItemImageFactory</a> performs a GDI stretch blit. If the caller wants a higher quality image stretch than provided through that mechanism, they should pass this flag and perform the stretch themselves.



#### SIIGBF_MEMORYONLY (0x00000002)

Return the item only if it is already in memory. Do not access the disk even if the item is cached. Note that this only returns an already-cached icon and can fall back to a per-class icon if an item has a per-instance icon that has not been cached. Retrieving a thumbnail, even if it is cached, always requires the disk to be accessed, so <b>GetImage</b> should not be called from the UI thread without passing <b>SIIGBF_MEMORYONLY</b>.



#### SIIGBF_ICONONLY (0x00000004)

Return only the icon, never the thumbnail.



#### SIIGBF_THUMBNAILONLY (0x00000008)

Return only the thumbnail, never the icon. Note that not all items have thumbnails, so <b>SIIGBF_THUMBNAILONLY</b> will cause the method to fail in these cases.



#### SIIGBF_INCACHEONLY (0x00000010)

Allows access to the disk, but only to retrieve a cached item. This returns a cached thumbnail if it is available. If no cached thumbnail is available, it returns a cached per-instance icon but does not extract a thumbnail or icon.



#### SIIGBF_CROPTOSQUARE (0x00000020)

<b>Introduced in Windows 8</b>. If necessary, crop the bitmap to a square.



#### SIIGBF_WIDETHUMBNAILS (0x00000040)

<b>Introduced in Windows 8</b>. Stretch and crop the bitmap to a 0.7 aspect ratio.



#### SIIGBF_ICONBACKGROUND (0x00000080)

<b>Introduced in Windows 8</b>. If returning an icon, paint a background using the associated app's registered background color.



#### SIIGBF_SCALEUP (0x00000100)

<b>Introduced in Windows 8</b>. If necessary, stretch the bitmap so that the height and width fit the given size.


### -param phbm [out]

Type: <b>HBITMAP*</b>

Pointer to a value that, when this method returns successfully, receives the handle of the retrieved bitmap. It is the responsibility of the caller to free this retrieved resource through <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Icon extraction can be time consuming. This method generally should not be called from a UI thread to avoid causing that thread to become unresponsive. You can call <b>IShellItemImageFactory::GetImage</b> on a UI thread if you set the <b>SIIGBF_INCACHEONLY</b> flag. However, if the image is not found in the cache, the calling application should be prepared to launch a background thread to extract the image. An extraction should never be done on a UI thread.

See the <a href="https://msdn.microsoft.com/63B1D242-A52A-4796-90D7-A5AC8E3002B4">Using Image Factory</a> sample for a full example of how to use this method.



