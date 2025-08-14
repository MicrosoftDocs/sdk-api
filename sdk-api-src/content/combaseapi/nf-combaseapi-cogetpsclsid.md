---
UID: NF:combaseapi.CoGetPSClsid
title: CoGetPSClsid function (combaseapi.h)
description: Returns the CLSID of the DLL that implements the proxy and stub for the specified interface.
helpviewer_keywords: ["CoGetPSClsid","CoGetPSClsid function [COM]","_com_CoGetPSClsid","com.cogetpsclsid","combaseapi/CoGetPSClsid"]
old-location: com\cogetpsclsid.htm
tech.root: com
ms.assetid: dfe6b514-a80a-4adb-bf43-d9a7d0e5f4a3
ms.date: 12/05/2018
ms.keywords: CoGetPSClsid, CoGetPSClsid function [COM], _com_CoGetPSClsid, com.cogetpsclsid, combaseapi/CoGetPSClsid
req.header: combaseapi.h
req.include-header: Objbase.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoGetPSClsid
 - combaseapi/CoGetPSClsid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetPSClsid
---

# CoGetPSClsid function


## -description

Returns the CLSID of the DLL that implements the proxy and stub for the specified interface.

## -parameters

### -param riid [in]

The interface whose proxy/stub CLSID is to be returned.

### -param pClsid [out]

Specifies where to store the proxy/stub CLSID for the interface specified by <i>riid</i>.

## -returns

This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The proxy/stub CLSID was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete this operation.

</td>
</tr>
</table>

## -remarks

The <b>CoGetPSClsid</b> function looks at the <b>HKEY_CLASSES_ROOT</b>&#92;<b>Interfaces</b>&#92;<i>{string form of riid}</i>&#92;<b>ProxyStubClsid32</b> key in the registry to determine the CLSID of the DLL to load in order to create the proxy and stub for the interface specified by <i>riid</i>. This function also returns the CLSID for any interface IID registered by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterpsclsid">CoRegisterPSClsid</a> within the current process.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterpsclsid">CoRegisterPSClsid</a>