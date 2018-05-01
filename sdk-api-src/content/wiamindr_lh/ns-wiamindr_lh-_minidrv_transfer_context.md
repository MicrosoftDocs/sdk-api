---
UID: NS:wiamindr_lh._MINIDRV_TRANSFER_CONTEXT
title: "_MINIDRV_TRANSFER_CONTEXT"
author: windows-driver-content
description: The MINIDRV_TRANSFER_CONTEXT structure is used to store image and other information needed for a memory-callback data transfer or a file data transfer.
old-location: image\minidrv_transfer_context.htm
old-project: image
ms.assetid: 26583873-4f84-4254-86c1-2063df85000c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PMINIDRV_TRANSFER_CONTEXT, MINIDRV_TRANSFER_CONTEXT, MINIDRV_TRANSFER_CONTEXT structure [Imaging Devices], PMINIDRV_TRANSFER_CONTEXT, PMINIDRV_TRANSFER_CONTEXT structure pointer [Imaging Devices], _MINIDRV_TRANSFER_CONTEXT, image.minidrv_transfer_context, wiamindr_lh/MINIDRV_TRANSFER_CONTEXT, wiamindr_lh/PMINIDRV_TRANSFER_CONTEXT, wiastrct_36e477d2-73a8-41b7-af46-82fb7c6f0bca.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: MINIDRV_TRANSFER_CONTEXT, *PMINIDRV_TRANSFER_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiamindr_lh.h
api_name:
-	MINIDRV_TRANSFER_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _MINIDRV_TRANSFER_CONTEXT structure


## -description


The MINIDRV_TRANSFER_CONTEXT structure is used to store image and other information needed for a memory-callback data transfer or a file data transfer.


## -struct-fields




### -field lSize

Specifies the size in bytes of this MINIDRV_TRANSFER_CONTEXT structure.


### -field lWidthInPixels

Specifies the width in pixels of the current image. The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551615">WIA_IPA_PIXELS_PER_LINE</a> common item property.


### -field lLines

Specifies the total number of lines (the number of horizontal rows of pixels) in the current image. The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551611">WIA_IPA_NUMBER_OF_LINES</a> common item property.


### -field lDepth

Specifies the color depth value of the current image in bits per pixel. The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551546">WIA_IPA_DEPTH</a> common item property.


### -field lXRes

Specifies the current horizontal resolution of the image in pixels per inch. The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552665">WIA_IPS_XRES</a> scanner item property.


### -field lYRes

Specifies the current vertical resolution of the image in pixels per inch. The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552673">WIA_IPS_YRES</a> scanner item property.


### -field lCompression

Specifies the type of compression used by the device. The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551540">WIA_IPA_COMPRESSION</a> common item property.


### -field guidFormatID

Specifies a GUID that indicates the data format for the device. The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551553">WIA_IPA_FORMAT</a> common item property.


### -field tymed

Specifies the type of data transfer. The data transfer specified can be either a memory-callback transfer (TYMED_CALLBACK or TYMED_MULTIPAGE_CALLBACK) or file transfer (TYMED_FILE or TYMED_MULTIPAGE_FILE). The value of this member is derived from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551656">WIA_IPA_TYMED</a> common item property. 

This member conveys information related to that in the <b>bTransferDataCB</b> member. See <b>Remarks</b> for more information.


### -field hFile

Specifies the handle to the open file used during file transfers. The minidriver should not use this member. See <b>Remarks</b> for more information.


### -field cbOffset

Specifies the current offset in bytes of the next buffer location used during this transfer.


### -field lBufferSize

Specifies the total size of the transfer buffer.


### -field lActiveBuffer

Specifies which buffer is used for the current transfer. The value of this member must be in the range of 1 through <b>lNumBuffers</b>.


### -field lNumBuffers

Specifies the number of buffers available for data transfer. This value can currently be either 1 or 2.


### -field pBaseBuffer

Points to the start of the base transfer buffer.


### -field pTransferBuffer

Points to the start of the current transfer buffer. For a callback transfer in which double buffering is used, this member alternates between the two buffers, pointing to the beginning of the first buffer, and then to the beginning of the second, and so on.


### -field bTransferDataCB

Specifies whether a data transfer is a memory-callback transfer or a file transfer. This member is set to <b>TRUE</b> if the transfer is a memory-callback transfer, and <b>FALSE</b> if the transfer is a file transfer. For file transfers, the WIA service usually provides a callback routine, which enables the application to receive updates from the minidriver about the status of the file transfer. (The WIA service provides a callback routine if the application provides its own callback routine. See <a href="https://msdn.microsoft.com/a535d718-e34f-4cd0-9137-83d28d0b8e9c">IWiaMiniDrvCallback COM Interface</a> for details.) For file transfers, a minidriver should check the value stored in the <b>pIWiaMiniDrvCallBack</b> member. If that member is <b>NULL</b>, the WIA service does not provide a callback routine, so the driver must not attempt to call it. For memory-callback transfers, the WIA service always provides a callback.

This member conveys information related to that in the <b>tymed</b> member. See <b>Remarks</b> for more information.


### -field bClassDrvAllocBuf

Specifies whether the WIA service has allocated the transfer buffer. This value is <b>TRUE</b> if the WIA service allocated the buffer, and <b>FALSE</b> if not. In that case, it is the minidriver's responsibility to allocate the transfer buffer.


### -field lClientAddress

Specifies the address, in the client's address space, of the transfer. The minidriver must not change this value.


### -field pIWiaMiniDrvCallBack

Points to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff543943">IWiaMiniDrvCallBack Interface</a> used for data or status callback transfer.


### -field lImageSize

Specifies the size, in bytes, of uncompressed bits in a single page.


### -field lHeaderSize

Specifies the size, in bytes, of image header data in a single page.


### -field lItemSize

Specifies the size, in bytes, of bits and header. This value can be zero if the item size is unknown before acquisition.


### -field cbWidthInBytes

Specifies the size, in bytes, of an image line.


### -field lPage

Specifies the page number of the current page when scanning a multipage TIFF image. Page numbering begins with zero.


### -field lCurIfdOffset

Specifies the image file directory (IFD) offset in the current page of a multipage TIFF image.


### -field lPrevIfdOffset

Specifies the image file directory (IFD) offset in the previous page of a multipage TIFF image.


## -remarks



The WIA service sets most of the members of this structure before it calls the minidriver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff543956">IWiaMiniDrv::drvAcquireItemData</a> method. If the minidriver calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff549249">wiasGetImageInformation</a>, then that function fills in the remaining members of the MINIDRV_TRANSFER_CONTEXT passed to it.

Because the WIA service currently uses only the TYMED_FILE and TYMED_CALLBACK constants, the <b>tymed</b> and <b>bTransferDataCB</b> members store essentially the same information. For file transfers, when <b>bTransferDataCB</b> is set to <b>FALSE</b>, <b>tymed</b> is set to either TYMED_FILE or TYMED_MULTIPAGE_FILE. For memory-callback transfers, when <b>bTransferDataCB</b> is set to <b>TRUE</b>, <b>tymed</b> is set to either TYMED_CALLBACK or TYMED_MULTIPAGE_CALLBACK.

The <b>hFile</b> member is reserved for use solely by the WIA service. Rather than using this member for file transfers, the minidriver should instead write the data to a buffer, and then call <a href="https://msdn.microsoft.com/library/windows/hardware/ff549484">wiasWritePageBufToFile</a> to complete the file transfer.

The minidriver obtains values from specific common or scanner item properties to set the members shown in the following table:

<table>
<tr>
<th rowspan="2">Member</th>
<th>Common or Scanner Item Property</th>
</tr>
<tr>
<th>Used to Set this Member</th>
</tr>
<tr>
<td>
<b>lWidthInPixels</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff551615">WIA_IPA_PIXELS_PER_LINE</a>


</td>
</tr>
<tr>
<td>
<b>lLines</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff551611">WIA_IPA_NUMBER_OF_LINES</a>


</td>
</tr>
<tr>
<td>
<b>lDepth</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff551546">WIA_IPA_DEPTH</a>


</td>
</tr>
<tr>
<td>
<b>lXRes</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff552665">WIA_IPS_XRES</a>


</td>
</tr>
<tr>
<td>
<b>lYRes</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff552673">WIA_IPS_YRES</a>


</td>
</tr>
<tr>
<td>
<b>lCompression</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff551540">WIA_IPA_COMPRESSION</a>


</td>
</tr>
<tr>
<td>
<b>guidFormatID</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff551553">WIA_IPA_FORMAT</a>


</td>
</tr>
<tr>
<td>
<b>tymed</b>

</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff551656">WIA_IPA_TYMED</a>


</td>
</tr>
</table>
 

Usually, the minidriver sets the preceding structure members directly from the values of the item properties. An application or the minidriver will have set the item properties earlier. The WIA service fills in its service context, using the property values. The driver can use the values stored in this context for quick reference.

The WIA service sets the following structure members:

<ul>
<li>
<b>hFile</b>

</li>
<li>
<b>bTransferDataCB</b>

</li>
<li>
<b>bClassDrvAllocBuf</b>

</li>
</ul>
Either the minidriver or the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549249">wiasGetImageInformation</a> service library function sets the following structure members:

<ul>
<li>
<b>lImageSize</b>

</li>
<li>
<b>lHeaderSize</b>

</li>
<li>
<b>lItemSize</b>

</li>
<li>
<b>cbWidthInBytes</b>

</li>
</ul>
The following members of this structure are used in data transfer callbacks. The WIA service or the minidriver sets these members. In several cases, the value stored in <b>bClassDrvAllocBuf</b> determines whether the WIA service or the minidriver sets the member.

<table>
<tr>
<th>Member</th>
<th>Set by?</th>
</tr>
<tr>
<td>
<b>cbOffset</b>

</td>
<td>
Minidriver

</td>
</tr>
<tr>
<td>
<b>lBufferSize</b>

</td>
<td>
WIA service or minidriver

If <b>bClassDrvAllocBuf</b> is <b>TRUE</b>, the WIA service sets this member; otherwise, the minidriver sets it.

</td>
</tr>
<tr>
<td>
<b>lActiveBuffer</b>

</td>
<td>
WIA service

The minidriver must not modify this member.

</td>
</tr>
<tr>
<td>
<b>lNumBuffers</b>

</td>
<td>
WIA service

The minidriver must not modify this member.

</td>
</tr>
<tr>
<td>
<b>pBaseBuffer</b>

</td>
<td>
WIA service or minidriver

If <b>bClassDrvAllocBuf</b> is <b>TRUE</b>, the WIA service sets this member; otherwise, the minidriver sets it.

</td>
</tr>
<tr>
<td>
<b>pTransferBuffer</b>

</td>
<td>
WIA service or minidriver

If <b>bClassDrvAllocBuf</b> is <b>TRUE</b>, the WIA service sets this member; otherwise, the minidriver sets it.

</td>
</tr>
<tr>
<td>
<b>lClientAddress</b>

</td>
<td>
WIA service

The minidriver must not modify this member.

</td>
</tr>
<tr>
<td>
<b>pIWiaMiniDrvCallBack</b>

</td>
<td>
WIA service

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543956">IWiaMiniDrv::drvAcquireItemData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543946">IWiaMiniDrvCallBack::MiniDrvCallback</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549249">wiasGetImageInformation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549484">wiasWritePageBufToFile</a>
 

 

