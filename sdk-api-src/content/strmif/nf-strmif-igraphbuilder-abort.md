---
UID: NF:strmif.IGraphBuilder.Abort
title: IGraphBuilder::Abort (strmif.h)
author: windows-sdk-content
description: The Abort method requests the Filter Graph Manager to halt its current task as quickly as possible.
old-location: dshow\igraphbuilder_abort.htm
tech.root: DirectShow
ms.assetid: e9a46959-afa0-4e12-80c3-c4b95feb96e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Abort, Abort method [DirectShow], Abort method [DirectShow],IGraphBuilder interface, IGraphBuilder interface [DirectShow],Abort method, IGraphBuilder.Abort, IGraphBuilder::Abort, IGraphBuilderAbort, dshow.igraphbuilder_abort, strmif/IGraphBuilder::Abort
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
 - IGraphBuilder.Abort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphBuilder::Abort


## -description



The <code>Abort</code> method requests the Filter Graph Manager to halt its current task as quickly as possible.



The current task may or may not fail to complete. Possibly the fastest option for the Filter Graph Manager is to complete the task.


## -parameters






## -returns



Returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder Interface</a>
 

 

