---
UID: NF:sdoias.ISdoMachine.GetDictionarySDO
title: ISdoMachine::GetDictionarySDO (sdoias.h)
description: The GetDictionarySDO method retrieves an interface for an attribute-dictionary SDO.
helpviewer_keywords: ["GetDictionarySDO","GetDictionarySDO method [Network Policy Server]","GetDictionarySDO method [Network Policy Server]","ISdoMachine interface","GetDictionarySDO method [Network Policy Server]","SdoMachine object","ISdoMachine interface [Network Policy Server]","GetDictionarySDO method","ISdoMachine.GetDictionarySDO","ISdoMachine::GetDictionarySDO","SdoMachine object [Network Policy Server]","GetDictionarySDO method","_sdo_isdomachine_getdictionarysdo","nps.SDO_isdomachine_getdictionarysdo","sdo.isdomachine_getdictionarysdo","sdoias/ISdoMachine::GetDictionarySDO"]
old-location: nps\SDO_isdomachine_getdictionarysdo.htm
tech.root: Nps
ms.assetid: 172444be-b2a2-4060-af92-b0c63f0ffe6b
ms.date: 12/05/2018
ms.keywords: GetDictionarySDO, GetDictionarySDO method [Network Policy Server], GetDictionarySDO method [Network Policy Server],ISdoMachine interface, GetDictionarySDO method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetDictionarySDO method, ISdoMachine.GetDictionarySDO, ISdoMachine::GetDictionarySDO, SdoMachine object [Network Policy Server],GetDictionarySDO method, _sdo_isdomachine_getdictionarysdo, nps.SDO_isdomachine_getdictionarysdo, sdo.isdomachine_getdictionarysdo, sdoias/ISdoMachine::GetDictionarySDO
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdoMachine::GetDictionarySDO
 - sdoias/ISdoMachine::GetDictionarySDO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoMachine.GetDictionarySDO
 - SdoMachine.GetDictionarySDO
---

# ISdoMachine::GetDictionarySDO


## -description

The 
<b>GetDictionarySDO</b> method retrieves an interface for an attribute-dictionary SDO.

## -parameters

### -param ppDictionarySDO [out]

Pointer to an ISdoDictionary.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Before calling this method, use the 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a> method to attach to the SDO computer.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold">ISdoDictionaryOld</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine">ISdoMachine</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a>