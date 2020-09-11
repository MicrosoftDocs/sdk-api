---
UID: NN:shimgdata.IShellImageData
title: IShellImageData (shimgdata.h)
description: Exposes methods and properties that display, manipulate, and describe image data.
helpviewer_keywords: ["IShellImageData","IShellImageData interface [Windows Shell]","IShellImageData interface [Windows Shell]","described","_shell_IShellImageData","shell.IShellImageData","shimgdata/IShellImageData"]
old-location: shell\IShellImageData.htm
tech.root: shell
ms.assetid: 935e651c-4dcd-4317-847e-34adf656035c
ms.date: 12/05/2018
ms.keywords: IShellImageData, IShellImageData interface [Windows Shell], IShellImageData interface [Windows Shell],described, _shell_IShellImageData, shell.IShellImageData, shimgdata/IShellImageData
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageData
 - shimgdata/IShellImageData
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
 - IShellImageData
---

# IShellImageData interface


## -description

<p class="CCE_Message">[This interface will eventually be unsupported. It is recommended that Windows GDI+ APIs be used in place of <b>IShellImageData</b> methods.]

Exposes methods and properties that display, manipulate, and describe image data.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellImageData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellImageData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellImageData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-cloneframe">CloneFrame</a>
</td>
<td align="left" width="63%">
Retrieves a clone of the current image or frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">Decode</a>
</td>
<td align="left" width="63%">
Decodes the image file, setting state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-discardedit">DiscardEdit</a>
</td>
<td align="left" width="63%">
Discards edits made to an image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-displayname">DisplayName</a>
</td>
<td align="left" width="63%">
Gets the name of the file if <b>IShellImageData</b> was initialized on a file path. Otherwise, gets the name of the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-draw">Draw</a>
</td>
<td align="left" width="63%">
Draws a decoded image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getcurrentpage">GetCurrentPage</a>
</td>
<td align="left" width="63%">
Gets the current page of a multipage image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getdelay">GetDelay</a>
</td>
<td align="left" width="63%">
Gets the delay value for the current frame of an animation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getencoderparams">GetEncoderParams</a>
</td>
<td align="left" width="63%">
Gets the current set of encoder parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getpagecount">GetPageCount</a>
</td>
<td align="left" width="63%">
Gets the number of pages in a multipage image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getpixelformat">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Gets the pixel format of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> through which the properties of the image can be accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getrawdataformat">GetRawDataFormat</a>
</td>
<td align="left" width="63%">
Retrieves a GUID that identifies the format of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getresolution">GetResolution</a>
</td>
<td align="left" width="63%">
Gets the resolution, in dpi, of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Gets the dimensions of the image file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-isanimated">IsAnimated</a>
</td>
<td align="left" width="63%">
Determines whether the image is animated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-isdecoded">IsDecoded</a>
</td>
<td align="left" width="63%">
Determines whether the image has been decoded by calling <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">IShellImageData::Decode</a>. Many operations return a failure code if the image is not first decoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-iseditable">IsEditable</a>
</td>
<td align="left" width="63%">
Determines whether the image can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-ismultipage">IsMultipage</a>
</td>
<td align="left" width="63%">
Determines whether the image is a multipage TIFF image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-isprintable">IsPrintable</a>
</td>
<td align="left" width="63%">
Determines whether the image can be printed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-istransparent">IsTransparent</a>
</td>
<td align="left" width="63%">
Determines whether the image is transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-isvector">IsVector</a>
</td>
<td align="left" width="63%">
Determines whether the image is a vector image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-nextframe">NextFrame</a>
</td>
<td align="left" width="63%">
Switches to the next frame of an animated image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-nextpage">NextPage</a>
</td>
<td align="left" width="63%">
Switches to the next page of a multipage image. Any associated animations are reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-prevpage">PrevPage</a>
</td>
<td align="left" width="63%">
Switches to the previous page of a multipage image. Any associated animations are reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-registerabort">RegisterAbort</a>
</td>
<td align="left" width="63%">
Sets a callback abort object, optionally returning a pointer to the previous object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-replaceframe">ReplaceFrame</a>
</td>
<td align="left" width="63%">
Replaces the current frame with a new image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-rotate">Rotate</a>
</td>
<td align="left" width="63%">
Rotates an image in increments of 90 degrees.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-scale">Scale</a>
</td>
<td align="left" width="63%">
Adjusts the size of an image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-selectpage">SelectPage</a>
</td>
<td align="left" width="63%">
Selects a specified page in a multipage image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-setencoderparams">SetEncoderParams</a>
</td>
<td align="left" width="63%">
Sets encoder parameters.

</td>
</tr>
</table>

## -remarks

This interface was not included in a public header file prior to Windows Vista.

