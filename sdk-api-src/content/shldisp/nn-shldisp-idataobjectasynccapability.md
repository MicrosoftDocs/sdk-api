---
UID: NN:shldisp.IDataObjectAsyncCapability
title: IDataObjectAsyncCapability (shldisp.h)
description: Enables interfaces that are usually synchronous to function asynchronously.
helpviewer_keywords: ["IDataObjectAsyncCapability","IDataObjectAsyncCapability interface [Windows Shell]","IDataObjectAsyncCapability interface [Windows Shell]","described","shell.IDataObjectAsyncCapability","shldisp/IDataObjectAsyncCapability"]
old-location: shell\IDataObjectAsyncCapability.htm
tech.root: shell
ms.assetid: 2E23A137-0C5B-4ce9-8100-758C7E17753B
ms.date: 12/05/2018
ms.keywords: IDataObjectAsyncCapability, IDataObjectAsyncCapability interface [Windows Shell], IDataObjectAsyncCapability interface [Windows Shell],described, shell.IDataObjectAsyncCapability, shldisp/IDataObjectAsyncCapability
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataObjectAsyncCapability
 - shldisp/IDataObjectAsyncCapability
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDataObjectAsyncCapability
---

# IDataObjectAsyncCapability interface


## -description

Enables interfaces that are usually synchronous to function asynchronously.
        
            
<div class="alert"><b>Note</b>  This interface is the current, renamed version of <a href="/previous-versions/bb776309(v=vs.85)">IAsyncOperation</a>.</div><div> </div>

## -inheritance

The <b>IDataObjectAsyncCapability</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataObjectAsyncCapability</b> also has these types of members:

## -remarks

<b>IDataObjectAsyncCapability</b> is an optional interface that is implemented by a data object. It allows the drop target to negotiate with the drop source to extract data from the data object asynchronously.

This interface is primarily exported by the data objects used with drag-and-drop and Clipboard operations. Typically, such operations are synchronous. However, if data rendering will be time-consuming, <b>IDataObjectAsyncCapability</b> can be used to allow data extraction to take place on a background thread. See the <i>Dragging and Dropping Shell Objects Asynchronously</i> section of <a href="/windows/desktop/shell/datascenarios">Handling Shell Data Transfer Scenarios</a> for a detailed discussion of how to use this interface.

Drop sources and targets use this interface when they wish to have a lengthy data extraction process handled by a background thread.
