---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# __MIDL___MIDL_itf_ctffunc_0000_0011_0001 enumeration


## -description


Elements of the <b>TfSapiObject</b> enumeration are used with the <a href="https://msdn.microsoft.com/4dfa2bd2-e25c-4481-ab07-2f764434504d">ITfFnGetSAPIObject::Get</a> method to specify a specific type of Speech API (SAPI) object.


## -enum-fields




### -field GETIF_RESMGR

Specifies an ISpResourceManager object.


### -field GETIF_RECOCONTEXT

Specifies an ISpRecoContext object.


### -field GETIF_RECOGNIZER

Specifies an ISpRecognizer object.


### -field GETIF_VOICE

Specifies an ISpVoice object.


### -field GETIF_DICTGRAM

Specifies an ISpRecoGrammar object.


### -field GETIF_RECOGNIZERNOINIT

Specifies an ISpRecognizer object. SAPI will not be initialized if it is not already.


## -see-also




<a href="https://msdn.microsoft.com/4dfa2bd2-e25c-4481-ab07-2f764434504d">ITfFnGetSAPIObject::Get
      </a>
 

 

