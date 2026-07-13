---
UID: NF:shobjidl_core.IShellItemImageFactory.GetImage
title: IShellItemImageFactory::GetImage (shobjidl_core.h)
description: Gets an HBITMAP that represents an IShellItem.
helpviewer_keywords: ["GetImage","GetImage method [Windows Shell]","GetImage method [Windows Shell]","IShellItemImageFactory interface","IShellItemImageFactory interface [Windows Shell]","GetImage method","IShellItemImageFactory.GetImage","IShellItemImageFactory::GetImage","SIIGBF_BIGGERSIZEOK","SIIGBF_CROPTOSQUARE","SIIGBF_ICONBACKGROUND","SIIGBF_ICONONLY","SIIGBF_INCACHEONLY","SIIGBF_MEMORYONLY","SIIGBF_RESIZETOFIT","SIIGBF_SCALEUP","SIIGBF_THUMBNAILONLY","SIIGBF_WIDETHUMBNAILS","_shell_IShellItemImageFactory_GetImage","shell.IShellItemImageFactory_GetImage","shobjidl_core/IShellItemImageFactory::GetImage"]
old-location: shell\IShellItemImageFactory_GetImage.htm
tech.root: shell
ms.assetid: b31a5eb7-f12f-41e0-9047-450240371424
ms.date: 12/05/2018
ms.keywords: GetImage, GetImage method [Windows Shell], GetImage method [Windows Shell],IShellItemImageFactory interface, IShellItemImageFactory interface [Windows Shell],GetImage method, IShellItemImageFactory.GetImage, IShellItemImageFactory::GetImage, SIIGBF_BIGGERSIZEOK, SIIGBF_CROPTOSQUARE, SIIGBF_ICONBACKGROUND, SIIGBF_ICONONLY, SIIGBF_INCACHEONLY, SIIGBF_MEMORYONLY, SIIGBF_RESIZETOFIT, SIIGBF_SCALEUP, SIIGBF_THUMBNAILONLY, SIIGBF_WIDETHUMBNAILS, _shell_IShellItemImageFactory_GetImage, shell.IShellItemImageFactory_GetImage, shobjidl_core/IShellItemImageFactory::GetImage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemImageFactory::GetImage
 - shobjidl_core/IShellItemImageFactory::GetImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemImageFactory.GetImage
---

# IShellItemImageFactory::GetImage


## -description

Gets an <b>HBITMAP</b> that represents an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>. The default behavior is to load a thumbnail. If there is no thumbnail for the current <b>IShellItem</b>, it retrieves an <b>HBITMAP</b> for the icon of the item. The thumbnail or icon is extracted if it is not currently cached.

## -parameters

### -param size [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a></b>

A structure that specifies the size of the image to be received.

### -param flags [in]

Type: <b>SIIGBF</b>

One or more of the following:



#### SIIGBF_RESIZETOFIT (0x00000000)

Shrink the bitmap as necessary to fit, preserving its aspect ratio.



#### SIIGBF_BIGGERSIZEOK (0x00000001)

Passed by callers if they want to stretch the returned image themselves. For example, if the caller passes an icon size of 80x80, a 96x96 thumbnail could be returned. This action can be used as a performance optimization if the caller expects that they will need to stretch the image. Note that the Shell implementation of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory">IShellItemImageFactory</a> performs a GDI stretch blit. If the caller wants a higher quality image stretch than provided through that mechanism, they should pass this flag and perform the stretch themselves.



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

Pointer to a value that, when this method returns successfully, receives the handle of the retrieved bitmap. It is the responsibility of the caller to free this retrieved resource through <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Icon extraction can be time consuming. This method generally should not be called from a UI thread to avoid causing that thread to become unresponsive. You can call <b>IShellItemImageFactory::GetImage</b> on a UI thread if you set the <b>SIIGBF_INCACHEONLY</b> flag. However, if the image is not found in the cache, the calling application should be prepared to launch a background thread to extract the image. An extraction should never be done on a UI thread.

See the <a href="/windows/win32/shell/samples-usingimagefactory">Using Image Factory</a> sample for a full example of how to use this method.
