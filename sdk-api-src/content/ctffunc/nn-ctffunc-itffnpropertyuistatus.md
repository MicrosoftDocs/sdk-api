---
UID: NN:ctffunc.ITfFnPropertyUIStatus
title: ITfFnPropertyUIStatus (ctffunc.h)
description: The ITfFnPropertyUIStatus interface is implemented by a text service and used by an application or text service to obtain and set the status of the text service property UI.
helpviewer_keywords: ["ITfFnPropertyUIStatus","ITfFnPropertyUIStatus interface [Text Services Framework]","ITfFnPropertyUIStatus interface [Text Services Framework]","described","_tsf_itffnpropertyuistatus_ref","ctffunc/ITfFnPropertyUIStatus","tsf.itffnpropertyuistatus"]
old-location: tsf\itffnpropertyuistatus.htm
tech.root: TSF
ms.assetid: 5583ae98-02a5-4303-9674-b8a85b52442a
ms.date: 12/05/2018
ms.keywords: ITfFnPropertyUIStatus, ITfFnPropertyUIStatus interface [Text Services Framework], ITfFnPropertyUIStatus interface [Text Services Framework],described, _tsf_itffnpropertyuistatus_ref, ctffunc/ITfFnPropertyUIStatus, tsf.itffnpropertyuistatus
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfFnPropertyUIStatus
 - ctffunc/ITfFnPropertyUIStatus
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
 - ITfFnPropertyUIStatus
---

# ITfFnPropertyUIStatus interface


## -description

The <b>ITfFnPropertyUIStatus</b> interface is implemented by a text service and used by an application or text service to obtain and set the status of the text service property UI.

An application or text service obtains an instance of this interface by obtaining the <a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> for the text service and calling <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> with IID_ITfFnPropertyUIStatus.

## -inheritance

The <b>ITfFnPropertyUIStatus</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnPropertyUIStatus</b> also has these types of members:

