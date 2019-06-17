---
UID: NF:strmif.IAMovieSetup.Register
title: IAMovieSetup::Register (strmif.h)
author: windows-sdk-content
description: Note  The IAMovieSetup interface is deprecated. Use the AMovieDllRegisterServer2 function instead. Adds the filter to the registry.
old-location: dshow\iamoviesetup_register.htm
tech.root: DirectShow
ms.assetid: c39edba2-df48-43e4-9a0d-d5c409a8a9d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMovieSetup interface [DirectShow],Register method, IAMovieSetup.Register, IAMovieSetup::Register, IAMovieSetupRegister, Register, Register method [DirectShow], Register method [DirectShow],IAMovieSetup interface, dshow.iamoviesetup_register, strmif/IAMovieSetup::Register
ms.topic: method
f1_keywords: ["strmif/IAMovieSetup.Register"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMovieSetup.Register
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMovieSetup::Register


## -description



<div class="alert"><b>Note</b>  The <b>IAMovieSetup</b> interface is deprecated. Use the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/amoviedllregisterserver2">AMovieDllRegisterServer2</a> function instead.</div>
<div> </div>
Adds the filter to the registry.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method registers the filter, its pins, and the media type associated with the pins. It should be implemented to use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper</a> methods to accomplish this. See the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasefilter-register">CBaseFilter::Register</a> member function for a description of its implementation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamoviesetup">IAMovieSetup Interface</a>
 

 

