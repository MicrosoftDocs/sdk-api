---
UID: NF:strmif.IGraphBuilder.Abort
title: IGraphBuilder::Abort (strmif.h)
description: The Abort method requests the Filter Graph Manager to halt its current task as quickly as possible.
helpviewer_keywords: ["Abort","Abort method [DirectShow]","Abort method [DirectShow]","IGraphBuilder interface","IGraphBuilder interface [DirectShow]","Abort method","IGraphBuilder.Abort","IGraphBuilder::Abort","IGraphBuilderAbort","dshow.igraphbuilder_abort","strmif/IGraphBuilder::Abort"]
old-location: dshow\igraphbuilder_abort.htm
tech.root: dshow
ms.assetid: e9a46959-afa0-4e12-80c3-c4b95feb96e5
ms.date: 12/05/2018
ms.keywords: Abort, Abort method [DirectShow], Abort method [DirectShow],IGraphBuilder interface, IGraphBuilder interface [DirectShow],Abort method, IGraphBuilder.Abort, IGraphBuilder::Abort, IGraphBuilderAbort, dshow.igraphbuilder_abort, strmif/IGraphBuilder::Abort
f1_keywords:
- strmif/IGraphBuilder.Abort
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGraphBuilder::Abort


## -description



The <code>Abort</code> method requests the Filter Graph Manager to halt its current task as quickly as possible.



The current task may or may not fail to complete. Possibly the fastest option for the Filter Graph Manager is to complete the task.


## -parameters






## -returns



Returns S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder Interface</a>
 

 

