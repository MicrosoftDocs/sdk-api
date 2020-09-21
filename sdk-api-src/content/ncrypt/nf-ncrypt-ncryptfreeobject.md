---
UID: NF:ncrypt.NCryptFreeObject
title: NCryptFreeObject function (ncrypt.h)
description: Frees a CNG key storage object.
helpviewer_keywords: ["NCryptFreeObject","NCryptFreeObject function [Security]","ncrypt/NCryptFreeObject","security.ncryptfreeobject_func"]
old-location: security\ncryptfreeobject_func.htm
tech.root: security
ms.assetid: a5535cf9-ba8c-4212-badd-f1dc88903624
ms.date: 12/05/2018
ms.keywords: NCryptFreeObject, NCryptFreeObject function [Security], ncrypt/NCryptFreeObject, security.ncryptfreeobject_func
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptFreeObject
 - ncrypt/NCryptFreeObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptFreeObject
---

# NCryptFreeObject function


## -description

The <b>NCryptFreeObject</b> function frees a CNG key storage object.

## -parameters

### -param hObject [in]

The handle of the object to free. This can be either a provider handle (<b>NCRYPT_PROV_HANDLE</b>) or a key handle (<b>NCRYPT_KEY_HANDLE</b>).

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hObject</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenstorageprovider">NCryptOpenStorageProvider</a>