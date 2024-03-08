---
UID: NE:ctffunc.__MIDL___MIDL_itf_ctffunc_0000_0011_0001
title: TfSapiObject (ctffunc.h)
description: Elements of the TfSapiObject enumeration are used with the ITfFnGetSAPIObject::Get method to specify a specific type of Speech API (SAPI) object.
helpviewer_keywords: ["GETIF_DICTGRAM","GETIF_RECOCONTEXT","GETIF_RECOGNIZER","GETIF_RECOGNIZERNOINIT","GETIF_RESMGR","GETIF_VOICE","TfSapiObject","TfSapiObject enumeration [Text Services Framework]","_tsf_tfsapiobject_ref","ctffunc/GETIF_DICTGRAM","ctffunc/GETIF_RECOCONTEXT","ctffunc/GETIF_RECOGNIZER","ctffunc/GETIF_RECOGNIZERNOINIT","ctffunc/GETIF_RESMGR","ctffunc/GETIF_VOICE","ctffunc/TfSapiObject","tsf.tfsapiobject"]
old-location: tsf\tfsapiobject.htm
tech.root: TSF
ms.assetid: 82fb6417-efee-4f04-a9a9-4e52934e2e86
ms.date: 12/05/2018
ms.keywords: GETIF_DICTGRAM, GETIF_RECOCONTEXT, GETIF_RECOGNIZER, GETIF_RECOGNIZERNOINIT, GETIF_RESMGR, GETIF_VOICE, TfSapiObject, TfSapiObject enumeration [Text Services Framework], _tsf_tfsapiobject_ref, ctffunc/GETIF_DICTGRAM, ctffunc/GETIF_RECOCONTEXT, ctffunc/GETIF_RECOGNIZER, ctffunc/GETIF_RECOGNIZERNOINIT, ctffunc/GETIF_RESMGR, ctffunc/GETIF_VOICE, ctffunc/TfSapiObject, tsf.tfsapiobject
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TfSapiObject
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ctffunc_0000_0011_0001
 - ctffunc/__MIDL___MIDL_itf_ctffunc_0000_0011_0001
 - TfSapiObject
 - ctffunc/TfSapiObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ctffunc.h
api_name:
 - TfSapiObject
---

# TfSapiObject enumeration


## -description

Elements of the <b>TfSapiObject</b> enumeration are used with the <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffngetsapiobject-get">ITfFnGetSAPIObject::Get</a> method to specify a specific type of Speech API (SAPI) object.

## -enum-fields

### -field GETIF_RESMGR:0

Specifies an ISpResourceManager object.

### -field GETIF_RECOCONTEXT:0x1

Specifies an ISpRecoContext object.

### -field GETIF_RECOGNIZER:0x2

Specifies an ISpRecognizer object.

### -field GETIF_VOICE:0x3

Specifies an ISpVoice object.

### -field GETIF_DICTGRAM:0x4

Specifies an ISpRecoGrammar object.

### -field GETIF_RECOGNIZERNOINIT:0x5

Specifies an ISpRecognizer object. SAPI will not be initialized if it is not already.

## -see-also

<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffngetsapiobject-get">ITfFnGetSAPIObject::Get
      </a>
