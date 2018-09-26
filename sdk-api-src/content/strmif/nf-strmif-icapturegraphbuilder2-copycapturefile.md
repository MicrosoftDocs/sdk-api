---
UID: NF:strmif.ICaptureGraphBuilder2.CopyCaptureFile
title: ICaptureGraphBuilder2::CopyCaptureFile
author: windows-sdk-content
description: The CopyCaptureFile method copies the valid media data from a capture file.
old-location: dshow\icapturegraphbuilder2_copycapturefile.htm
tech.root: DirectShow
ms.assetid: d4084b12-b082-45c2-9f07-625b980c7e4c
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CopyCaptureFile, CopyCaptureFile method [DirectShow], CopyCaptureFile method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],CopyCaptureFile method, ICaptureGraphBuilder2.CopyCaptureFile, ICaptureGraphBuilder2::CopyCaptureFile, ICaptureGraphBuilder2CopyCaptureFile, dshow.icapturegraphbuilder2_copycapturefile, strmif/ICaptureGraphBuilder2::CopyCaptureFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICaptureGraphBuilder2.CopyCaptureFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICaptureGraphBuilder2::CopyCaptureFile


## -description



The <code>CopyCaptureFile</code> method copies the valid media data from a capture file.




## -parameters




### -param lpwstrOld [in]

Pointer to a wide-character string that contains the source file name.


### -param lpwstrNew [in]

Pointer to a wide-character string that contains the destination file name. Valid data is copied to this file.


### -param fAllowEscAbort [in]

Boolean value that specifies whether pressing the ESC key cancels the copy operation. If the value is <b>TRUE</b> and the user presses the ESC key, the operation halts. If the value is <b>FALSE</b>, the method ignores the ESC key.


### -param pCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/780ffe63-f4b6-4b3c-b7a6-571b58aba4dd">IAMCopyCaptureFileProgress</a> interface to display progress information, or <b>NULL</b>. See Remarks for more information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
User canceled the operation before it completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Could not open the source file or destination file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



Typically, you will first capture to a large preallocated file. This method copies just the valid data to a new file. As a result, the new file can be much smaller than the original file.

The source and destination files must be AVI files. Other file types are not supported.

To display the progress of the copy operation, implement the <a href="https://msdn.microsoft.com/780ffe63-f4b6-4b3c-b7a6-571b58aba4dd">IAMCopyCaptureFileProgress</a> interface and pass a pointer to the interface in the <i>pCallback</i> parameter. If <i>pCallback</i> is non-<b>NULL</b>, this method periodically calls the <a href="https://msdn.microsoft.com/6908627e-51de-4206-bdb2-b3aaedf9478f">IAMCopyCaptureFileProgress::Progress</a> method with an integer between 0 and 100 that specifies the percentage complete.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2 Interface</a>
 

 

