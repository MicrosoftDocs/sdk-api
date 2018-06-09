---
UID: NF:strmif.IGraphBuilder.SetLogFile
title: IGraphBuilder::SetLogFile
author: windows-sdk-content
description: The SetLogFile method sets the file for logging actions taken when attempting to perform an operation.
old-location: dshow\igraphbuilder_setlogfile.htm
old-project: DirectShow
ms.assetid: 194960ee-3418-420f-9242-a372097e4dc9
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IGraphBuilder interface [DirectShow],SetLogFile method, IGraphBuilder.SetLogFile, IGraphBuilder::SetLogFile, IGraphBuilderSetLogFile, SetLogFile, SetLogFile method [DirectShow], SetLogFile method [DirectShow],IGraphBuilder interface, dshow.igraphbuilder_setlogfile, strmif/IGraphBuilder::SetLogFile
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
 - IGraphBuilder.SetLogFile
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphBuilder::SetLogFile


## -description



The <code>SetLogFile</code> method sets the file for logging actions taken when attempting to perform an operation.




## -parameters




### -param hFile

Handle to the log file.


## -returns



Returns S_OK.




## -remarks



This method is for use in debugging; it is intended to help you determine the cause of any failure to automatically build a filter graph.

The <i>hFile</i> parameter must be an open file handle. Your application is responsible for opening the file and for closing it when you are done logging. Before closing the file handle, call <code>SetLogFile</code> with a <b>NULL</b> file handle. This will ensure that the component does not attempt to use the file handle after you have closed it.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder Interface</a>
 

 

