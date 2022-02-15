---
UID: NF:strmif.IAMovieSetup.Unregister
title: IAMovieSetup::Unregister (strmif.h)
description: Note  The IAMovieSetup interface is deprecated. Use the AMovieDllRegisterServer2 function instead. Removes the filter from the registry.
helpviewer_keywords: ["IAMovieSetup interface [DirectShow]","Unregister method","IAMovieSetup.Unregister","IAMovieSetup::Unregister","IAMovieSetupUnregister","Unregister","Unregister method [DirectShow]","Unregister method [DirectShow]","IAMovieSetup interface","dshow.iamoviesetup_unregister","strmif/IAMovieSetup::Unregister"]
old-location: dshow\iamoviesetup_unregister.htm
tech.root: dshow
ms.assetid: 96266aef-f1ef-4b75-9d2e-e574f76fdec7
ms.date: 12/05/2018
ms.keywords: IAMovieSetup interface [DirectShow],Unregister method, IAMovieSetup.Unregister, IAMovieSetup::Unregister, IAMovieSetupUnregister, Unregister, Unregister method [DirectShow], Unregister method [DirectShow],IAMovieSetup interface, dshow.iamoviesetup_unregister, strmif/IAMovieSetup::Unregister
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMovieSetup::Unregister
 - strmif/IAMovieSetup::Unregister
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMovieSetup.Unregister
---

# IAMovieSetup::Unregister


## -description

<div class="alert"><b>Note</b>  The <b>IAMovieSetup</b> interface is deprecated. Use the <a href="/windows/desktop/DirectShow/amoviedllregisterserver2">AMovieDllRegisterServer2</a> function instead.</div>
<div> </div>
Removes the filter from the registry.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method should be implemented to use the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltermapper-unregisterfilter">IFilterMapper::UnregisterFilter</a> method to remove the filter from the registry. This effectively removes the pins and media types as well.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamoviesetup">IAMovieSetup Interface</a>
