---
UID: NN:strmif.IFileSinkFilter
title: IFileSinkFilter (strmif.h)
description: The IFileSinkFilter interface is implemented on filters that write media streams to a file.
helpviewer_keywords: ["IFileSinkFilter","IFileSinkFilter interface [DirectShow]","IFileSinkFilter interface [DirectShow]","described","IFileSinkFilterInterface","dshow.ifilesinkfilter","strmif/IFileSinkFilter"]
old-location: dshow\ifilesinkfilter.htm
tech.root: dshow
ms.assetid: aa1d3f8e-9790-4442-ba7e-896981bf1b96
ms.date: 12/05/2018
ms.keywords: IFileSinkFilter, IFileSinkFilter interface [DirectShow], IFileSinkFilter interface [DirectShow],described, IFileSinkFilterInterface, dshow.ifilesinkfilter, strmif/IFileSinkFilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSinkFilter
 - strmif/IFileSinkFilter
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
 - IFileSinkFilter
---

# IFileSinkFilter interface


## -description

The <code>IFileSinkFilter</code> interface is implemented on filters that write media streams to a file. A file sink filter in a video capture filter graph, for instance, writes the output of the video compression filter to a file. Typically, the application running this filter graph should enable the user to enter the name of the file to be written to. This interface enables the communication of this information.

If a filter needs the name of an output file, it should expose this interface to allow an application to set the file name. Note that there is currently no base class implementation of this interface.

Any application that must set the name of the file into which the file sink filter will write should use this interface to get and set the file name.

## -inheritance

The <b>IFileSinkFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileSinkFilter</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter2">IFileSinkFilter2</a> interface extends <b>IFileSinkFilter</b>.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
