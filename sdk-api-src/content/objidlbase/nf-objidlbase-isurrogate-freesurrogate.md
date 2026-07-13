---
UID: NF:objidlbase.ISurrogate.FreeSurrogate
title: ISurrogate::FreeSurrogate (objidlbase.h)
description: The ISurrogate::FreeSurrogate (objidlbase.h) method unloads a DLL server.
helpviewer_keywords: ["FreeSurrogate","FreeSurrogate method [COM]","FreeSurrogate method [COM]","ISurrogate interface","ISurrogate interface [COM]","FreeSurrogate method","ISurrogate.FreeSurrogate","ISurrogate::FreeSurrogate","_com_isurrogate_freesurrogate","com.isurrogate_freesurrogate","objidlbase/ISurrogate::FreeSurrogate"]
old-location: com\isurrogate_freesurrogate.htm
tech.root: com
ms.assetid: d897b02a-2540-4274-a0e3-e5c9299104a2
ms.date: 08/15/2022
ms.keywords: FreeSurrogate, FreeSurrogate method [COM], FreeSurrogate method [COM],ISurrogate interface, ISurrogate interface [COM],FreeSurrogate method, ISurrogate.FreeSurrogate, ISurrogate::FreeSurrogate, _com_isurrogate_freesurrogate, com.isurrogate_freesurrogate, objidlbase/ISurrogate::FreeSurrogate
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ISurrogate::FreeSurrogate
 - objidlbase/ISurrogate::FreeSurrogate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISurrogate.FreeSurrogate
---

# ISurrogate::FreeSurrogate


## -description

Unloads a DLL server.



## -returns

This method can return the standard return values E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

COM calls <b>FreeSurrogate</b> when there are no more DLL servers running in the surrogate process. When <b>FreeSurrogate</b> is called, the method must properly revoke all of the class factories registered in the surrogate, and then cause the surrogate process to exit.

Surrogate processes must call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a> function periodically to unload DLL servers that are no longer in use. The surrogate process assumes this responsibility, which would normally be the client's responsibility. <b>CoFreeUnusedLibraries</b> calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DllCanUnloadNow</a> function on any loaded DLL servers. Because <b>CoFreeUnusedLibraries</b> depends on the existence and proper implementation of <b>DllCanUnloadNow</b> in DLL servers, it is not guaranteed to unload all DLL servers that should be unloaded --not every server implements <b>DllCanUnloadNow</b>, and this function is unreliable for free-threaded DLLs. Additionally, the surrogate has no way of being informed when all DLL servers are gone. COM, however, can determine when all DLL servers have been unloaded, and will then call the <b>FreeSurrogate</b> method.

## -see-also

<a href="/windows/desktop/com/dllsurrogate">DllSurrogate</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isurrogate">ISurrogate</a>



<a href="/windows/desktop/com/writing-a-custom-surrogate">Writing a Custom Surrogate</a>
