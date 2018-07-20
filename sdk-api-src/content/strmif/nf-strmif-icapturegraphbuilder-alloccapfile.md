---
UID: NF:strmif.ICaptureGraphBuilder.AllocCapFile
title: ICaptureGraphBuilder::AllocCapFile
author: windows-sdk-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Preallocates a capture file to a specified size.
old-location: dshow\icapturegraphbuilder_alloccapfile.htm
old-project: DirectShow
ms.assetid: 116ee108-ae03-4761-84db-9391ebddaae2
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: AllocCapFile, AllocCapFile method [DirectShow], AllocCapFile method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],AllocCapFile method, ICaptureGraphBuilder.AllocCapFile, ICaptureGraphBuilder::AllocCapFile, ICaptureGraphBuilderAllocCapFile, dshow.icapturegraphbuilder_alloccapfile, strmif/ICaptureGraphBuilder::AllocCapFile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.AllocCapFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder::AllocCapFile


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Preallocates a capture file to a specified size.




## -parameters




### -param lpstr




### -param dwlSize






#### - dwSize [in]

Size, in bytes, of the file to be allocated.


#### - lpwstr [in]

Pointer to a wide-character string containing the name of the file to create or resize.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The call will fail if the file is read-only. For best capture results, always capture to a defragmented, preallocated capture file that is larger than the size of the capture data.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

