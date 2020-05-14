---
UID: NS:lpmapi.__unnamed_struct_34
title: ID_ERROR_OBJECT (lpmapi.h)
description: The ID_ERROR_OBJECT structure contains error message information for Identity Policy Elements for RSVP.helpviewer_keywords: ["ID_ERROR_OBJECT","ID_ERROR_OBJECT structure [QOS]","lpmapi/ID_ERROR_OBJECT","qos.id_error_object"]
old-location: qos\id_error_object.htm
tech.root: QOS
ms.assetid: de6e8eaa-4436-4b82-8c47-76da53116ff2
ms.date: 12/05/2018
ms.keywords: ID_ERROR_OBJECT, ID_ERROR_OBJECT structure [QOS], lpmapi/ID_ERROR_OBJECT, qos.id_error_object
f1_keywords:
- lpmapi/ID_ERROR_OBJECT
dev_langs:
- c++
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- HeaderDef
api_location:
- Lpmapi.h
api_name:
- ID_ERROR_OBJECT
targetos: Windows
req.typenames: ID_ERROR_OBJECT
req.redist: 
ms.custom: 19H1
---

# ID_ERROR_OBJECT structure


## -description


The 
<b>ID_ERROR_OBJECT</b> structure contains error message information for Identity Policy Elements for RSVP.


## -struct-fields




### -field usIdErrLength

Length of <b>udIdErrData</b>, in bytes.


### -field ucAType

Type of Identity Policy Element error. 


### -field ucSubType

Sub-type of the Identity Policy Element error.


### -field usReserved

Reserved. Do not use.


### -field usIdErrorValue

Value for the Identity Policy Element error.


### -field ucIdErrData

Identity Policy Element error data.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/qos/policy-elements">Policy Elements</a>
 

 

