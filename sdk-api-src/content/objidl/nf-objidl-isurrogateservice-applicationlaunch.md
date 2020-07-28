---
UID: NF:objidl.ISurrogateService.ApplicationLaunch
title: ISurrogateService::ApplicationLaunch (objidl.h)
description: Launches the application.
helpviewer_keywords: ["ApplicationLaunch","ApplicationLaunch method [COM]","ApplicationLaunch method [COM]","ISurrogateService interface","ISurrogateService interface [COM]","ApplicationLaunch method","ISurrogateService.ApplicationLaunch","ISurrogateService::ApplicationLaunch","_com_isurrogateservice_applicationlaunch","com.isurrogateservice_applicationlaunch","objidl/ISurrogateService::ApplicationLaunch"]
old-location: com\isurrogateservice_applicationlaunch.htm
tech.root: com
ms.assetid: 4e54c129-f321-4215-b084-21ab17f93a6f
ms.date: 12/05/2018
ms.keywords: ApplicationLaunch, ApplicationLaunch method [COM], ApplicationLaunch method [COM],ISurrogateService interface, ISurrogateService interface [COM],ApplicationLaunch method, ISurrogateService.ApplicationLaunch, ISurrogateService::ApplicationLaunch, _com_isurrogateservice_applicationlaunch, com.isurrogateservice_applicationlaunch, objidl/ISurrogateService::ApplicationLaunch
f1_keywords:
- objidl/ISurrogateService.ApplicationLaunch
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
- ObjIdl.h
api_name:
- ISurrogateService.ApplicationLaunch
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISurrogateService::ApplicationLaunch


## -description


Launches the application.


## -parameters




### -param rguidApplID [in]

The application identifier.


### -param appType [in]

The application type, as described in Remarks.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_UNEXPECTED.




## -remarks



The application type is defined by the following enum.

<pre class="syntax" xml:space="preserve"><code>typedef enum tagApplicationType { 
    ServerApplication, 
    LibraryApplication 
} ApplicationType;
</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-cogetinterceptor">CoGetInterceptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>



<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nn-callobj-icallframeevents">ICallFrameEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nn-callobj-icallinterceptor">ICallInterceptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nn-callobj-icallunmarshal">ICallUnmarshal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isurrogateservice">ISurrogateService</a>
 

 

