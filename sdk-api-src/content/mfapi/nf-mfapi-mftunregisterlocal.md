---
UID: NF:mfapi.MFTUnregisterLocal
title: MFTUnregisterLocal function (mfapi.h)
description: Unregisters one or more Media Foundation transforms (MFTs) from the caller's process.
helpviewer_keywords: ["MFTUnregisterLocal","MFTUnregisterLocal function [Media Foundation]","mf.mftunregisterlocal","mfapi/MFTUnregisterLocal"]
old-location: mf\mftunregisterlocal.htm
tech.root: mf
ms.assetid: e77edce7-0abb-41a3-a65e-fd159173e135
ms.date: 12/05/2018
ms.keywords: MFTUnregisterLocal, MFTUnregisterLocal function [Media Foundation], mf.mftunregisterlocal, mfapi/MFTUnregisterLocal
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFTUnregisterLocal
 - mfapi/MFTUnregisterLocal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFTUnregisterLocal
---

# MFTUnregisterLocal function


## -description

Unregisters one or more Media Foundation transforms (MFTs) from the caller's process.

## -parameters

### -param pClassFactory [in]

A pointer to the <b>IClassFactory</b> interface of a class factory object. This parameter can be <b>NULL</b>.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The MFT specified by the <i>pClassFactory</i> parameter was not registered in this process.

</td>
</tr>
</table>

## -remarks

Use this function to unregister a local MFT that was previously registered through the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal">MFTRegisterLocal</a> function.

If the <i>pClassFactory</i> parameter is <b>NULL</b>, all local MFTs in the process are unregistered. Otherwise, the function unregisters the MFT associated with the class factory specified by the <i>pClassFactory</i> parameter. In that case, the <i>pClassFactory</i> parameter should equal a pointer value that was previously passed to  the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal">MFTRegisterLocal</a> function.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>