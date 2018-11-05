---
UID: NF:strmif.IAMCopyCaptureFileProgress.Progress
title: IAMCopyCaptureFileProgress::Progress
author: windows-sdk-content
description: The Progress method is called periodically by the ICaptureGraphBuilder2::CopyCaptureFile method while it copies the file.
old-location: dshow\iamcopycapturefileprogress_progress.htm
tech.root: DirectShow
ms.assetid: 6908627e-51de-4206-bdb2-b3aaedf9478f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMCopyCaptureFileProgress interface [DirectShow],Progress method, IAMCopyCaptureFileProgress.Progress, IAMCopyCaptureFileProgress::Progress, IAMCopyCaptureFileProgressProgress, Progress, Progress method [DirectShow], Progress method [DirectShow],IAMCopyCaptureFileProgress interface, dshow.iamcopycapturefileprogress_progress, strmif/IAMCopyCaptureFileProgress::Progress
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
 - IAMCopyCaptureFileProgress.Progress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMCopyCaptureFileProgress::Progress


## -description



The <code>Progress</code> method is called periodically by the <a href="https://msdn.microsoft.com/d4084b12-b082-45c2-9f07-625b980c7e4c">ICaptureGraphBuilder2::CopyCaptureFile</a> method while it copies the file.




## -parameters




### -param iProgress [in]

Specifies the percentage of the copy operation that has completed, as a value between 0 and 100.


## -returns



Returns S_OK or an <b>HRESULT</b> error code.




## -remarks



Applications typically use the value of <i>iProgress</i> to update a progress bar on the user interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/780ffe63-f4b6-4b3c-b7a6-571b58aba4dd">IAMCopyCaptureFileProgress Interface</a>
 

 

