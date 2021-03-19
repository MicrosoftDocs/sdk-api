---
UID: NF:faxext.FaxExtInitializeConfig
title: FaxExtInitializeConfig function (faxext.h)
description: The fax service calls the FaxExtInitializeConfig function to initialize the fax extension DLL. The service calls this function before it calls any other fax extension initialization function.
helpviewer_keywords: ["FaxExtInitializeConfig","FaxExtInitializeConfig function [Fax Service]","_mfax_faxextinitializeconfig","fax._mfax_faxextinitializeconfig","faxext/FaxExtInitializeConfig"]
old-location: fax\_mfax_faxextinitializeconfig.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxextconfigref_15lz.htm
ms.date: 12/05/2018
ms.keywords: FaxExtInitializeConfig, FaxExtInitializeConfig function [Fax Service], _mfax_faxextinitializeconfig, fax._mfax_faxextinitializeconfig, faxext/FaxExtInitializeConfig
req.header: faxext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxExtInitializeConfig
 - faxext/FaxExtInitializeConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxExt.h
api_name:
 - FaxExtInitializeConfig
---

# FaxExtInitializeConfig function


## -description

The fax service calls the <b>FaxExtInitializeConfig</b> function to initialize the fax extension DLL. The service calls this function before it calls any other fax extension initialization function.

## -parameters

### -param unnamedParam1 [in]

Type: <b>PFAX_EXT_GET_DATA</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextgetdata">FaxExtGetData</a> fax service callback function.

### -param unnamedParam2 [in]

Type: <b>PFAX_EXT_SET_DATA</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextsetdata">FaxExtSetData</a> fax service callback function.

### -param unnamedParam3 [in]

Type: <b>PFAX_EXT_REGISTER_FOR_EVENTS</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextregisterforevents">FaxExtRegisterForEvents</a> fax service callback function.

### -param unnamedParam4 [in]

Type: <b>PFAX_EXT_UNREGISTER_FOR_EVENTS</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextunregisterforevents">FaxExtUnregisterForEvents</a> fax service callback function.

### -param unnamedParam5 [in]

Type: <b>PFAX_EXT_FREE_BUFFER</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextfreebuffer">FaxExtFreeBuffer</a> fax service callback function.

## -returns

Type: <b>HRESULT</b>

If the function succeeds, the return value is <b>NOERROR</b>.





If the fax extension DLL returns a value other than <b>NOERROR</b>, the fax service considers the extension to be in an error state. Even if other extension initialization functions succeed, the fax service does not recognize the extension.

## -remarks

A fax extension DLL must export <b>FaxExtInitializeConfig</b> if it plans to implement the fax extension configuration mechanism and receive notifications from the fax service about changes in device configuration data.

The <b>FaxExtInitializeConfig</b> function exposes pointers to the callback functions that the fax service supplies. The fax extension DLL must store these pointers in a global variable for later use.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextfreebuffer">FaxExtFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextgetdata">FaxExtGetData</a>



<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextregisterforevents">FaxExtRegisterForEvents</a>



<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextsetdata">FaxExtSetData</a>



<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextunregisterforevents">FaxExtUnregisterForEvents</a>