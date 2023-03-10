---
UID: NF:control.IMediaControl.RenderFile
title: IMediaControl::RenderFile (control.h)
description: The RenderFile method builds a filter graph that renders the specified file. (IMediaControl.RenderFile)
helpviewer_keywords: ["IMediaControl interface [DirectShow]","RenderFile method","IMediaControl.RenderFile","IMediaControl::RenderFile","IMediaControlRenderFile","RenderFile","RenderFile method [DirectShow]","RenderFile method [DirectShow]","IMediaControl interface","control/IMediaControl::RenderFile","dshow.imediacontrol_renderfile"]
old-location: dshow\imediacontrol_renderfile.htm
tech.root: dshow
ms.assetid: 5dfff776-da3f-40a3-86d4-76a5099d6e6f
ms.date: 12/05/2018
ms.keywords: IMediaControl interface [DirectShow],RenderFile method, IMediaControl.RenderFile, IMediaControl::RenderFile, IMediaControlRenderFile, RenderFile, RenderFile method [DirectShow], RenderFile method [DirectShow],IMediaControl interface, control/IMediaControl::RenderFile, dshow.imediacontrol_renderfile
req.header: control.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaControl::RenderFile
 - control/IMediaControl::RenderFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaControl.RenderFile
---

# IMediaControl::RenderFile


## -description

The <code>RenderFile</code> method builds a filter graph that renders the specified file.



This method is intended for use by Visual Basic 6.0 applications. It was documented for Visual Basic 6.0 as the <b>FilgraphManager.RenderFile</b> method. C++ applications should use the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a> method instead.

## -parameters

### -param strFilename [in]

Specifies the name of the file to load.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>
