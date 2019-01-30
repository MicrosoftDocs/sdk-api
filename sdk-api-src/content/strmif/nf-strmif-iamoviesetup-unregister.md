---
UID: NF:strmif.IAMovieSetup.Unregister
title: IAMovieSetup::Unregister
author: windows-sdk-content
description: Note  The IAMovieSetup interface is deprecated. Use the AMovieDllRegisterServer2 function instead. Removes the filter from the registry.
old-location: dshow\iamoviesetup_unregister.htm
tech.root: DirectShow
ms.assetid: 96266aef-f1ef-4b75-9d2e-e574f76fdec7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMovieSetup interface [DirectShow],Unregister method, IAMovieSetup.Unregister, IAMovieSetup::Unregister, IAMovieSetupUnregister, Unregister, Unregister method [DirectShow], Unregister method [DirectShow],IAMovieSetup interface, dshow.iamoviesetup_unregister, strmif/IAMovieSetup::Unregister
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
 - IAMovieSetup.Unregister
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMovieSetup::Unregister


## -description



<div class="alert"><b>Note</b>  The <b>IAMovieSetup</b> interface is deprecated. Use the <a href="https://msdn.microsoft.com/2122949d-0117-4c68-bfcd-c717b14dc970">AMovieDllRegisterServer2</a> function instead.</div>
<div> </div>
Removes the filter from the registry.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method should be implemented to use the <a href="https://msdn.microsoft.com/9b5941d4-d0e7-4f4a-b273-e0fa4a1e1c2e">IFilterMapper::UnregisterFilter</a> method to remove the filter from the registry. This effectively removes the pins and media types as well.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b200dbee-bab7-43d7-a204-751592fa2405">IAMovieSetup Interface</a>
 

 

