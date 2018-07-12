---
UID: NF:strmif.ICaptureGraphBuilder2.AllocCapFile
title: ICaptureGraphBuilder2::AllocCapFile
author: windows-sdk-content
description: The AllocCapFile method preallocates a capture file to a specified size. For best results, always capture to a defragmented, preallocated capture file that is larger than the size of the capture data.
old-location: dshow\icapturegraphbuilder2_alloccapfile.htm
old-project: DirectShow
ms.assetid: e61459bd-cccb-4857-b336-82d23135fa16
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: AllocCapFile, AllocCapFile method [DirectShow], AllocCapFile method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],AllocCapFile method, ICaptureGraphBuilder2.AllocCapFile, ICaptureGraphBuilder2::AllocCapFile, ICaptureGraphBuilder2AllocCapFile, dshow.icapturegraphbuilder2_alloccapfile, strmif/ICaptureGraphBuilder2::AllocCapFile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICaptureGraphBuilder2.AllocCapFile
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder2::AllocCapFile


## -description



The <code>AllocCapFile</code> method preallocates a capture file to a specified size. For best results, always capture to a defragmented, preallocated capture file that is larger than the size of the capture data.




## -parameters




### -param lpstr




### -param dwlSize [in]

Size of the file to allocate, in bytes.


#### - lpwstr [in]

Pointer to a wide-character string that contains the name of the file to create or resize.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method fails if the file is read-only.

It is best to allocate as much space as possible—ideally, more than needed. However, this can result in a very large file that contains relatively little data. For example, a 1-gigabyte (GB) capture file might contain a few megabytes of captured video. Use the <a href="https://msdn.microsoft.com/d4084b12-b082-45c2-9f07-625b980c7e4c">ICaptureGraphBuilder2::CopyCaptureFile</a> method to copy the data into a new file. That method copies only the data and ignores the empty portion of the original file.

If you use this method to preallocate the file, call <a href="https://msdn.microsoft.com/a32ae597-1468-4ac8-ae7b-8831d2a9ad6e">IFileSinkFilter2::SetMode</a> on the file-writer filter with the value zero. If the filter is set to AM_FILE_OVERWRITE, it will delete the preallocated file. Note that some file-writer filters do not support mode 0.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2 Interface</a>
 

 

