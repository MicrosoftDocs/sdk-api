---
UID: NF:shobjidl_core.IExtractImage.GetLocation
title: IExtractImage::GetLocation (shobjidl_core.h)
description: Gets a path to the image that is to be extracted.
helpviewer_keywords: ["GetLocation","GetLocation method [Windows Shell]","GetLocation method [Windows Shell]","IExtractImage interface","IEIFLAG_ASPECT","IEIFLAG_ASYNC","IEIFLAG_CACHE","IEIFLAG_GLEAM","IEIFLAG_NOBORDER","IEIFLAG_NOSTAMP","IEIFLAG_OFFLINE","IEIFLAG_ORIGSIZE","IEIFLAG_QUALITY","IEIFLAG_REFRESH","IEIFLAG_SCREEN","IEIT_PRIORITY_NORMAL","IEI_PRIORITY_MAX","IEI_PRIORITY_MIN","IExtractImage interface [Windows Shell]","GetLocation method","IExtractImage.GetLocation","IExtractImage::GetLocation","_win32_IExtractImage_GetLocation","shell.IExtractImage_GetLocation","shobjidl_core/IExtractImage::GetLocation"]
old-location: shell\IExtractImage_GetLocation.htm
tech.root: shell
ms.assetid: f1113429-ea89-4650-b345-db9e275232e6
ms.date: 12/05/2018
ms.keywords: GetLocation, GetLocation method [Windows Shell], GetLocation method [Windows Shell],IExtractImage interface, IEIFLAG_ASPECT, IEIFLAG_ASYNC, IEIFLAG_CACHE, IEIFLAG_GLEAM, IEIFLAG_NOBORDER, IEIFLAG_NOSTAMP, IEIFLAG_OFFLINE, IEIFLAG_ORIGSIZE, IEIFLAG_QUALITY, IEIFLAG_REFRESH, IEIFLAG_SCREEN, IEIT_PRIORITY_NORMAL, IEI_PRIORITY_MAX, IEI_PRIORITY_MIN, IExtractImage interface [Windows Shell],GetLocation method, IExtractImage.GetLocation, IExtractImage::GetLocation, _win32_IExtractImage_GetLocation, shell.IExtractImage_GetLocation, shobjidl_core/IExtractImage::GetLocation
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 4.70 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtractImage::GetLocation
 - shobjidl_core/IExtractImage::GetLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IExtractImage.GetLocation
---

# IExtractImage::GetLocation


## -description

Gets a path to the image that is to be extracted.

## -parameters

### -param pszPathBuffer [out]

Type: <b>LPWSTR</b>

The buffer used to return the path description. This value identifies the image so you can avoid loading the same one more than once.

### -param cch [in]

Type: <b>DWORD</b>

The size of <i>pszPathBuffer</i> in characters.

### -param pdwPriority [out]

Type: <b>DWORD*</b>

Not used.

<b>Microsoft Windows XP and earlier:</b> The pointer used to return the priority of the item when the <b>IEIFLAG_ASYNC</b> flag is set in <i>pdwFlags</i>. This parameter must not be <b>NULL</b>.  The function fails if this parameter is <b>NULL</b>, whether  <b>IEIFLAG_ASYNC</b> flag is set or not. 

This parameter is typically used to indicate the amount of time needed to extract the image. If you want more control over the order in which thumbnails are extracted, you can define multiple priority levels, up to 32 bits. As long as the integer values assigned to the different priority levels increase from low to high priority, the actual numbers you use aren't important. They are only used to determine the order in which the images will be extracted. There are three standard priority levels:



#### IEI_PRIORITY_MAX

Maximum priority.



#### IEI_PRIORITY_MIN

Minimum priority.



#### IEIT_PRIORITY_NORMAL

Normal priority.

<b>Microsoft Windows XP.</b> Not used.

### -param prgSize [in]

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure with the desired width and height of the image. Must not be <b>NULL</b>.

### -param dwRecClrDepth [in]

Type: <b>DWORD</b>

The recommended color depth in units of bits per pixel. Must not be <b>NULL</b>.

### -param pdwFlags [in, out]

Type: <b>DWORD*</b>

Flags that specify how the image is to be handled. Value must be one or more of the following:



#### IEIFLAG_ASPECT

Used to ask the object to use the supplied aspect ratio. If this flag is set, a rectangle with the desired aspect ratio will be passed in <i>prgSize</i>. This flag cannot be used with <b>IEIFLAG_SCREEN</b>.



#### IEIFLAG_ASYNC

Not used. The thumbnail is always extracted on a background thread.

<b>Microsoft Windows XP and earlier.</b> Used to ask if this instance supports asynchronous (free-threaded) extraction. If this flag is set by the calling applications, <b>IExtractImage::GetLocation</b> may return <b>E_PENDING</b>, indicating to the calling application to  extract the image on another thread. If <b>E_PENDING</b> is returned, the priority of the item is returned in <i>pdwPriority</i>.



#### IEIFLAG_CACHE

Not supported.

<b>Windows XP and earlier:</b> Set by the object to indicate that it will not cache the image. If this flag is returned, the Shell will cache a copy of the image.



#### IEIFLAG_GLEAM

Not supported.



#### IEIFLAG_NOBORDER (0x0100)

Not supported.



#### IEIFLAG_NOSTAMP (0x0080)

Not supported.



#### IEIFLAG_OFFLINE

Used to tell the object to use only local content for rendering.



#### IEIFLAG_ORIGSIZE


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Used to tell the object to render the image to the approximate size passed in <i>prgSize</i>, but crop it if necessary.



#### IEIFLAG_QUALITY (0x0200)

Passed to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-extract">IExtractImage::Extract</a> method to indicate that a higher quality image is requested.

If  this flag is not set, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a> retrieves an embedded thumbnail if the file has one, no matter what size the user requests. For example, if the file is 2000x2000 pixels but the embedded thumbnail is only 100x100 pixels and the user does not set this flag, yet requests a 1000x1000 pixel thumbnail, <b>IExtractImage</b> always returns the 100x100 pixel thumbnail. This is by design, since <b>IExtractImage</b> does not scale up. If a larger thumbnail is desired (usually embedded thumbnails are 160x160), this flag must be set.



#### IEIFLAG_REFRESH (0x0400)

Returned by the object to indicate that <b>Refresh Thumbnail</b> should be displayed on the item's shortcut menu.



#### IEIFLAG_SCREEN

Used to tell the object to render as if for the screen. This flag cannot be used with <b>IEIFLAG_ASPECT</b>.

## -returns

Type: <b>HRESULT</b>

This method may return a COM-defined error code or one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows XP and earlier:</b> If the <b>IEIFLAG_ASYNC</b> flag is set, this return value is used to indicate to the Shell that the object is free-threaded.

</td>
</tr>
</table>

## -remarks

<b>Microsoft Windows XP and earlier:</b> This method returns the path to an image and specifies how the image should be rendered. <b>IExtractImage::GetLocation</b> is free-threaded—that is, supports the Multithreaded Apartment Model (MTA)— therefore it can be placed in a background thread. The object must also expose an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask">IRunnableTask</a> interface, so the calling application can start and stop the extraction process as needed.

You should return images that fit within the boundaries defined by <i>prgSize</i>. With Windows 2000 and later systems, you can set <b>IEIFLAG_ORIGSIZE</b> to use objects that do not have a standard aspect ratio, and they will be displayed properly. You do not need to fill in the unused part of the rectangle. If you try to use a nonstandard aspect ratio image with earlier versions of the Shell, it will be stretched to fit the <i>prgSize</i> rectangle. Depending on how much the aspect ratio differs from what is specified, the image may be badly distorted.