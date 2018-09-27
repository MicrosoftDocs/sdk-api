---
UID: NF:strmif.ICaptureGraphBuilder.CopyCaptureFile
title: ICaptureGraphBuilder::CopyCaptureFile
author: windows-sdk-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Copies the valid media data from the preallocated capture file.
old-location: dshow\icapturegraphbuilder_copycapturefile.htm
tech.root: DirectShow
ms.assetid: 6eb4a3ed-6914-4839-ab1f-18510483ab49
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CopyCaptureFile, CopyCaptureFile method [DirectShow], CopyCaptureFile method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],CopyCaptureFile method, ICaptureGraphBuilder.CopyCaptureFile, ICaptureGraphBuilder::CopyCaptureFile, ICaptureGraphBuilderCopyCaptureFile, dshow.icapturegraphbuilder_copycapturefile, strmif/ICaptureGraphBuilder::CopyCaptureFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.CopyCaptureFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICaptureGraphBuilder::CopyCaptureFile


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Copies the valid media data from the preallocated capture file.




## -parameters




### -param lpwstrOld [in]

Pointer to a Unicode™ string containing the source file name.


### -param lpwstrNew [in]

Pointer to a Unicode string containing the destination file name. Valid data is copied to this file.


### -param fAllowEscAbort [in]

Value indicating whether pressing the ESC key will cancel the copy operation. <b>TRUE</b> indicates that it will; <b>FALSE</b> indicates that this method will ignore that keystroke.


### -param pCallback [in]

Optional pointer to an <a href="https://msdn.microsoft.com/780ffe63-f4b6-4b3c-b7a6-571b58aba4dd">IAMCopyCaptureFileProgress</a> show the progress (percentage complete) of the copy operation.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The new file will contain only valid data and therefore can be much shorter than the source file. Typically, you will always capture to the same huge preallocated file and use this method to copy the data you want to save from each capture to a new file.

If you specify <i>pCallback</i>, the <a href="https://msdn.microsoft.com/6908627e-51de-4206-bdb2-b3aaedf9478f">Progress</a> method on the <a href="https://msdn.microsoft.com/780ffe63-f4b6-4b3c-b7a6-571b58aba4dd">IAMCopyCaptureFileProgress</a> interface will be called periodically with an integer between 0 and 100 representing the percentage complete.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

