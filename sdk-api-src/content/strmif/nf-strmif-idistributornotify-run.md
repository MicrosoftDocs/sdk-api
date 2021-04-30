---
UID: NF:strmif.IDistributorNotify.Run
title: IDistributorNotify::Run (strmif.h)
description: The Run method is called when the filter graph is entering a running state.
helpviewer_keywords: ["IDistributorNotify interface [DirectShow]","Run method","IDistributorNotify.Run","IDistributorNotify::Run","IDistributorNotifyRun","Run","Run method [DirectShow]","Run method [DirectShow]","IDistributorNotify interface","dshow.idistributornotify_run","strmif/IDistributorNotify::Run"]
old-location: dshow\idistributornotify_run.htm
tech.root: dshow
ms.assetid: d6a6595b-b243-41bf-bba9-6e35fa81116c
ms.date: 12/05/2018
ms.keywords: IDistributorNotify interface [DirectShow],Run method, IDistributorNotify.Run, IDistributorNotify::Run, IDistributorNotifyRun, Run, Run method [DirectShow], Run method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_run, strmif/IDistributorNotify::Run
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
 - IDistributorNotify::Run
 - strmif/IDistributorNotify::Run
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
 - IDistributorNotify.Run
---

# IDistributorNotify::Run


## -description

The <code>Run</code> method is called when the filter graph is entering a running state.

## -parameters

### -param tStart

Stream-time offset that will be passed to every filter's <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-run">IMediaFilter::Run</a> method.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method is called before the filters are notified.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idistributornotify">IDistributorNotify Interface</a>