---
UID: NF:faxext.FaxExtFreeBuffer
title: FaxExtFreeBuffer function (faxext.h)
description: The FaxExtFreeBuffer callback function deallocates memory previously allocated by a successful call to the FaxExtGetData function.
helpviewer_keywords: ["FaxExtFreeBuffer","FaxExtFreeBuffer function [Fax Service]","_mfax_faxextfreebuffer","fax._mfax_faxextfreebuffer","faxext/FaxExtFreeBuffer"]
old-location: fax\_mfax_faxextfreebuffer.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxextconfigref_75bm.htm
ms.date: 12/05/2018
ms.keywords: FaxExtFreeBuffer, FaxExtFreeBuffer function [Fax Service], _mfax_faxextfreebuffer, fax._mfax_faxextfreebuffer, faxext/FaxExtFreeBuffer
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
 - FaxExtFreeBuffer
 - faxext/FaxExtFreeBuffer
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
 - FaxExtFreeBuffer
---

# FaxExtFreeBuffer function


## -description

The <b>FaxExtFreeBuffer</b> callback function deallocates memory previously allocated by a successful call to the <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextgetdata">FaxExtGetData</a> function.

## -parameters

### -param lpvBuffer

Type: <b>LPVOID</b>

Pointer to the data retrieved by a successful call to the <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextgetdata">FaxExtGetData</a> function.

## -remarks

When the fax extension calls this fax service callback function, it must use the function pointer exposed by the fax service when the service calls the <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextinitializeconfig">FaxExtInitializeConfig</a> function.

The fax service passes a pointer to the <b>FaxExtFreeBuffer</b> callback function when the fax service calls the <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextinitializeconfig">FaxExtInitializeConfig</a> function. The PFAX_EXT_FREE_BUFFER data type is a pointer to a <b>FaxExtFreeBuffer</b> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextgetdata">FaxExtGetData</a>



<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextinitializeconfig">FaxExtInitializeConfig</a>