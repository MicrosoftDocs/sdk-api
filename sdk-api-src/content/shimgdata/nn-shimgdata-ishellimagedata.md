---
UID: NN:shimgdata.IShellImageData
title: IShellImageData
author: windows-sdk-content
description: Exposes methods and properties that display, manipulate, and describe image data.
old-location: shell\IShellImageData.htm
tech.root: shell
ms.assetid: 935e651c-4dcd-4317-847e-34adf656035c
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IShellImageData, IShellImageData interface [Windows Shell], IShellImageData interface [Windows Shell],described, _shell_IShellImageData, shell.IShellImageData, shimgdata/IShellImageData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageData interface


## -description


<p class="CCE_Message">[This interface will eventually be unsupported. It is recommended that Windows GDI+ APIs be used in place of <b>IShellImageData</b> methods.]

Exposes methods and properties that display, manipulate, and describe image data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellImageData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellImageData</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/220d307a-7969-443c-963b-80132509ad8b">CloneFrame</a>
</td>
<td align="left" width="63%">
Retrieves a clone of the current image or frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">Decode</a>
</td>
<td align="left" width="63%">
Decodes the image file, setting state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bd16fa1-530d-46c7-bd1b-4ec9bf596881">DiscardEdit</a>
</td>
<td align="left" width="63%">
Discards edits made to an image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2e95a44-2bf7-43e1-9a29-950acc34d2a4">DisplayName</a>
</td>
<td align="left" width="63%">
Gets the name of the file if <b>IShellImageData</b> was initialized on a file path. Otherwise, gets the name of the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35989c3b-15b9-4503-a883-99df730b2a80">Draw</a>
</td>
<td align="left" width="63%">
Draws a decoded image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75489f7f-1ec5-471c-bc45-c8f480b0fa99">GetCurrentPage</a>
</td>
<td align="left" width="63%">
Gets the current page of a multipage image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5815771-7c96-4431-bc43-a5e620bd1d2f">GetDelay</a>
</td>
<td align="left" width="63%">
Gets the delay value for the current frame of an animation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b664d0f-7bb7-4cdd-8c0c-2ca80faaa764">GetEncoderParams</a>
</td>
<td align="left" width="63%">
Gets the current set of encoder parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5967a167-2cd5-4662-b624-e136c0092118">GetPageCount</a>
</td>
<td align="left" width="63%">
Gets the number of pages in a multipage image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43520cdd-66f1-4c75-bcec-7631de4f96c3">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Gets the pixel format of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fb59627-a31f-4c23-955f-3032c5814a5a">GetProperties</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> through which the properties of the image can be accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c09c6833-501d-4f27-9d59-3ca9aed9d0d1">GetRawDataFormat</a>
</td>
<td align="left" width="63%">
Retrieves a GUID that identifies the format of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e3c3e0f-010b-4d7d-a8fa-178a808687f8">GetResolution</a>
</td>
<td align="left" width="63%">
Gets the resolution, in dpi, of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50294d95-801d-4cd6-94ae-8b48c68af50f">GetSize</a>
</td>
<td align="left" width="63%">
Gets the dimensions of the image file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5b36862-5beb-4702-a5b3-feb70dc5e1ef">IsAnimated</a>
</td>
<td align="left" width="63%">
Determines whether the image is animated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f02dbf35-4dc7-4750-978d-b703338514df">IsDecoded</a>
</td>
<td align="left" width="63%">
Determines whether the image has been decoded by calling <a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">IShellImageData::Decode</a>. Many operations return a failure code if the image is not first decoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81dbb486-0b35-44ff-9aa2-2e449995591e">IsEditable</a>
</td>
<td align="left" width="63%">
Determines whether the image can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9c86f0e-5237-432c-a2bb-4054a23d707e">IsMultipage</a>
</td>
<td align="left" width="63%">
Determines whether the image is a multipage TIFF image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c50e919-cb5b-4332-bc17-ad24f31cf680">IsPrintable</a>
</td>
<td align="left" width="63%">
Determines whether the image can be printed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/613d2c01-47d5-41c3-8dba-5b1e1feabdf3">IsTransparent</a>
</td>
<td align="left" width="63%">
Determines whether the image is transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4099bc4-c831-4a4e-a3f6-932570dc8029">IsVector</a>
</td>
<td align="left" width="63%">
Determines whether the image is a vector image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b797539e-7766-4da7-864f-401c7c2ff082">NextFrame</a>
</td>
<td align="left" width="63%">
Switches to the next frame of an animated image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19a2680a-f435-45c9-9573-e32f3cfdd090">NextPage</a>
</td>
<td align="left" width="63%">
Switches to the next page of a multipage image. Any associated animations are reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3a4f07e-a1c0-4180-a02c-12eaebaaf1d2">PrevPage</a>
</td>
<td align="left" width="63%">
Switches to the previous page of a multipage image. Any associated animations are reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21ea1f3b-3b8a-4a92-a1fb-c19f0e97a407">RegisterAbort</a>
</td>
<td align="left" width="63%">
Sets a callback abort object, optionally returning a pointer to the previous object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f066c503-4512-46db-be50-016996b92668">ReplaceFrame</a>
</td>
<td align="left" width="63%">
Replaces the current frame with a new image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42fd8596-e130-4029-bf3c-67199e8dd804">Rotate</a>
</td>
<td align="left" width="63%">
Rotates an image in increments of 90 degrees.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebcc9cc1-b6ee-4fb9-9125-54d6a9ee9434">Scale</a>
</td>
<td align="left" width="63%">
Adjusts the size of an image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc852087-59f7-4c84-861a-e270a6ecf840">SelectPage</a>
</td>
<td align="left" width="63%">
Selects a specified page in a multipage image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20a5b0ab-5dcb-4ea9-9c15-d7c1e6c2c6be">SetEncoderParams</a>
</td>
<td align="left" width="63%">
Sets encoder parameters.

</td>
</tr>
</table> 


## -remarks



This interface was not included in a public header file prior to Windows Vista.



