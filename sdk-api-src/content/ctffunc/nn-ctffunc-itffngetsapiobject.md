---
UID: NN:ctffunc.ITfFnGetSAPIObject
title: ITfFnGetSAPIObject (ctffunc.h)
description: The ITfFnGetSAPIObject interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to obtain various SAPI objects.
helpviewer_keywords: ["ITfFnGetSAPIObject","ITfFnGetSAPIObject interface [Text Services Framework]","ITfFnGetSAPIObject interface [Text Services Framework]","described","_tsf_itffngetsapiobject_ref","ctffunc/ITfFnGetSAPIObject","tsf.itffngetsapiobject"]
old-location: tsf\itffngetsapiobject.htm
tech.root: TSF
ms.assetid: d7b4caa5-e915-4e57-878a-2a2d6ce609a7
ms.date: 12/05/2018
ms.keywords: ITfFnGetSAPIObject, ITfFnGetSAPIObject interface [Text Services Framework], ITfFnGetSAPIObject interface [Text Services Framework],described, _tsf_itffngetsapiobject_ref, ctffunc/ITfFnGetSAPIObject, tsf.itffngetsapiobject
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnGetSAPIObject
 - ctffunc/ITfFnGetSAPIObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnGetSAPIObject
---

# ITfFnGetSAPIObject interface


## -description

The <b>ITfFnGetSAPIObject</b> interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to obtain various SAPI objects.

A client obtains an instance of this interface by obtaining the <a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> for the SAPI text service and calling <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> with IID_ITfFnGetSAPIObject.

## -inheritance

The <b>ITfFnGetSAPIObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnGetSAPIObject</b> also has these types of members:

