---
UID: NN:imapi2fs.IBootOptions
title: IBootOptions
author: windows-sdk-content
description: Use this interface to specify the boot image to add to the optical disc. A boot image contains one or more sectors of code used to start the computer.
old-location: imapi\ibootoptions.htm
tech.root: imapi
ms.assetid: 446b535c-d576-4f96-8b74-305e34cb99d4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IBootOptions, IBootOptions interface [IMAPI], IBootOptions interface [IMAPI],described, imapi.ibootoptions, imapi2fs/IBootOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - imapi2fs.h
api_name:
 - IBootOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBootOptions interface


## -description


Use this interface to specify the boot image to add to the optical disc. A boot image contains one or more sectors of code used to start the computer.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(BootOptions) for the class identifier and __uuidof(IBootOptions) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBootOptions</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IBootOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBootOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63d598dd-72a8-4544-813d-11f2e7e53ec5">AssignBootImage</a>
</td>
<td align="left" width="63%">
Sets the data stream that contains the boot image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/161e0cea-63dd-4806-a246-4b36249b2cc7">get_BootImage</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the boot image data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ade69c2b-ff25-4993-bf4c-ee372e3cc1b0">get_Emulation</a>
</td>
<td align="left" width="63%">
Retrieves the media type that the boot image is intended to emulate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e3fd791-5a38-4082-9553-29eae92dfd5e">get_ImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the boot image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9c75760-42e8-4ad0-aa5c-82bfdc1327af">get_Manufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the manufacturer of the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d5ceb0e-4fd2-4146-8e15-b157c80a9d5b">get_PlatformId</a>
</td>
<td align="left" width="63%">
Retrieves the platform identifier that identifies the operating system architecture that the boot image supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93ed301e-fdea-451c-9ab0-6ea9a7fd45de">put_Emulation</a>
</td>
<td align="left" width="63%">
Sets the media type that the boot image is intended to emulate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/485b36f0-6c33-48da-8ac5-64f4fc13fd68">put_Manufacturer</a>
</td>
<td align="left" width="63%">
Sets an identifier that identifies the manufacturer of the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/295f3a3c-0f01-4b9b-b73c-48f075e6a33a">put_PlatformId</a>
</td>
<td align="left" width="63%">
Sets the platform identifier that identifies the operating system architecture that the boot image supports.

</td>
</tr>
</table> 


## -remarks



This interface supports the "El Torito" Bootable CD-ROM format specification. For details, see the specification at  <a href="Http://go.microsoft.com/fwlink/p/?linkid=84155">http://www.phoenix.com/NR/rdonlyres/98D3219C-9CC9-4DF5-B496-A286D893E36A/0/specscdrom.pdf</a>.

To add the boot image to a file system image, call the <a href="https://msdn.microsoft.com/0556b72d-eabd-4649-b16b-fd66052504f4">IFileSystemImage::put_BootImageOptions</a> method. 

To get the boot image associated with a file system image, call the <a href="https://msdn.microsoft.com/b9721313-a2b0-4d91-af10-7932bd2d01be">IFileSystemImage::get_BootImageOptions</a> method.

To create the <b>BootOptions</b> object in a script, use IMAPI2.BootOptions as the program identifier when calling <b>CreateObject</b>.



