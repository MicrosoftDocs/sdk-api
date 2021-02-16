---
UID: NF:objidl.ISurrogateService.ApplicationFree
title: ISurrogateService::ApplicationFree (objidl.h)
description: Releases the application.
helpviewer_keywords: ["ApplicationFree","ApplicationFree method [COM]","ApplicationFree method [COM]","ISurrogateService interface","ISurrogateService interface [COM]","ApplicationFree method","ISurrogateService.ApplicationFree","ISurrogateService::ApplicationFree","_com_isurrogateservice_applicationfree","com.isurrogateservice_applicationfree","objidl/ISurrogateService::ApplicationFree"]
old-location: com\isurrogateservice_applicationfree.htm
tech.root: com
ms.assetid: 703de030-ac99-4673-8399-695116bf07d5
ms.date: 12/05/2018
ms.keywords: ApplicationFree, ApplicationFree method [COM], ApplicationFree method [COM],ISurrogateService interface, ISurrogateService interface [COM],ApplicationFree method, ISurrogateService.ApplicationFree, ISurrogateService::ApplicationFree, _com_isurrogateservice_applicationfree, com.isurrogateservice_applicationfree, objidl/ISurrogateService::ApplicationFree
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISurrogateService::ApplicationFree
 - objidl/ISurrogateService::ApplicationFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - ISurrogateService.ApplicationFree
---

# ISurrogateService::ApplicationFree


## -description

Releases the application.

## -parameters

### -param rguidApplID [in]

The application identifier.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_UNEXPECTED.

## -see-also

<a href="/windows/desktop/api/callobj/nf-callobj-cogetinterceptor">CoGetInterceptor</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframeevents">ICallFrameEvents</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallinterceptor">ICallInterceptor</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallunmarshal">ICallUnmarshal</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isurrogateservice">ISurrogateService</a>