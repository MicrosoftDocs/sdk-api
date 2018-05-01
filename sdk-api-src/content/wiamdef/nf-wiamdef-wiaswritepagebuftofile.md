---
UID: NF:wiamdef.wiasWritePageBufToFile
title: wiasWritePageBufToFile function
author: windows-driver-content
description: The wiasWritePageBufToFile function writes the contents of a temporary page buffer to an image file.
old-location: image\wiaswritepagebuftofile.htm
old-project: image
ms.assetid: aa04ef8c-5b69-4d7e-8af4-8cbdb680a23a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaswritepagebuftofile, wiamdef/wiasWritePageBufToFile, wiasFncs_1d5b96b4-4737-481a-ae6a-e1ec4e8affef.xml, wiasWritePageBufToFile, wiasWritePageBufToFile function [Imaging Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wiaservc.dll
api_name:
-	wiasWritePageBufToFile
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasWritePageBufToFile function


## -description


The <b>wiasWritePageBufToFile </b>function writes the contents of a temporary page buffer to an image file.


## -parameters




### -param pmdtc [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



The function writes data from a minidriver-allocated temporary page buffer to the image file opened by the WIA service. Minidrivers typically call this function after acquiring a page of data for which the minidriver allocated a temporary buffer.

This function is similar to <a href="https://msdn.microsoft.com/library/windows/hardware/ff549473">wiasWriteBufToFile</a>, which can be used to write a buffer of image data to any type of image file. If a WIA minidriver intends to write a page of image data to a multipage TIFF file, including all appropriate tags, image file directory (IFD) entries, and other nonimage data, it should call this function, rather than <b>wiasWriteBufToFile</b>.

The expression <i>pmdtc</i>-&gt;<i>hFile</i> contains the handle to the file in TYMED_FILE (and TYMED_MULTIPAGE_FILE) transfers. This can be used to directly access the file that is being written to.

An example of how to use it is:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>SetFilePointer((HANDLE)(LONG_PTR)pmdtc-&gt;hFile,0,NULL,FILE_BEGIN);
if (!WriteFile((HANDLE)(LONG_PTR)pmdtc-&gt;hFile,
    pMyBuffer,
    dwNumBytesToWrite,
   &amp;dwNumBytesWritten,
    NULL)) {
     //
     // Some error happened
     // 
     .
     .
     .
    }</pre>
</td>
</tr>
</table></span></div>
However, if you are considering using just the file handle in your TYMED_FILE and TYMED_MULTIPAGE_FILE transfers (to write data directly to the file using the file handle, instead of calling <b>wiasWritePageBufToFile</b>), use <a href="https://msdn.microsoft.com/library/windows/hardware/ff549473">wiasWriteBufToFile</a>. This function performs the equivalent of:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>  bRet = WriteFile((HANDLE)ULongToPtr(pmdtc-&gt;hFile),
    pmdtc-&gt;pTransferBuffer,
    pmdtc-&gt;lItemSize,
    &amp;ulWritten,
    NULL);</pre>
</td>
</tr>
</table></span></div>
This is essentially what you would do if you used the file handle directly. The advantage of the first example is that if the implementation was changed in a future release of WIA (for example, if the WIA service began using pipes instead of files, internally), the driver would not need to be updated.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549473">wiasWriteBufToFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549495">wiasWritePageBufToStream</a>
 

 

