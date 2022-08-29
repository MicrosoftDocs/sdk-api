---
UID: NF:objidl.ISurrogate.LoadDllServer
title: ISurrogate::LoadDllServer (objidl.h)
description: The ISurrogate::LoadDllServer method (objidl.h) loads a DLL server into the implementing surrogate. 
helpviewer_keywords: ["ISurrogate interface [COM]","LoadDllServer method","ISurrogate.LoadDllServer","ISurrogate::LoadDllServer","LoadDllServer","LoadDllServer method [COM]","LoadDllServer method [COM]","ISurrogate interface","_com_isurrogate_loaddllserver","com.isurrogate_loaddllserver","objidlbase/ISurrogate::LoadDllServer"]
old-location: com\isurrogate_loaddllserver.htm
tech.root: com
ms.assetid: 18727dee-392d-4f88-b1de-35da8a5887b6
ms.date: 08/15/2022
ms.keywords: ISurrogate interface [COM],LoadDllServer method, ISurrogate.LoadDllServer, ISurrogate::LoadDllServer, LoadDllServer, LoadDllServer method [COM], LoadDllServer method [COM],ISurrogate interface, _com_isurrogate_loaddllserver, com.isurrogate_loaddllserver, objidlbase/ISurrogate::LoadDllServer
req.header: objidl.h
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
 - ISurrogate::LoadDllServer
 - objidl/ISurrogate::LoadDllServer
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
 - ISurrogate.LoadDllServer
---

# ISurrogate::LoadDllServer


## -description

Loads a DLL server into the implementing surrogate. COM calls this method when there is an activation request for the DLL server's class, if the class is registered as <a href="/windows/desktop/com/dllsurrogate">DllSurrogate</a>.

## -parameters

### -param Clsid [in]

The CLSID of the DLL server to be loaded.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -remarks

Upon receiving a load request through <b>LoadDllServer</b>, the surrogate must perform the following steps:

<ol>
<li>Create a class factory object that supports <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>, and <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>.</li>
<li>Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a> to register the new class factory object as the class factory for the requested CLSID.</li>
</ol>
This class factory's implementation of <a href="/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">IClassFactory::CreateInstance</a> will create an instance of the requested CLSID method by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a> to get the class factory which creates an actual object for the given CLSID.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate">CoRegisterSurrogate</a>



<a href="/windows/desktop/com/dllsurrogate">DllSurrogate</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isurrogate">ISurrogate</a>



<a href="/windows/desktop/com/writing-a-custom-surrogate">Writing a Custom Surrogate</a>
