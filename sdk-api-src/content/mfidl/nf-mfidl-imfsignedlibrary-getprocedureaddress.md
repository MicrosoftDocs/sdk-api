---
UID: NF:mfidl.IMFSignedLibrary.GetProcedureAddress
title: IMFSignedLibrary::GetProcedureAddress (mfidl.h)
description: Gets the procedure address of the specified function in the signed library.
helpviewer_keywords: ["GetProcedureAddress","GetProcedureAddress method [Media Foundation]","GetProcedureAddress method [Media Foundation]","IMFSignedLibrary interface","IMFSignedLibrary interface [Media Foundation]","GetProcedureAddress method","IMFSignedLibrary.GetProcedureAddress","IMFSignedLibrary::GetProcedureAddress","mf.imfsignedlibrary_getprocedureaddress","mfidl/IMFSignedLibrary::GetProcedureAddress"]
old-location: mf\imfsignedlibrary_getprocedureaddress.htm
tech.root: mf
ms.assetid: d32678b0-422d-4fe8-9bbc-fc203a39fdd5
ms.date: 12/05/2018
ms.keywords: GetProcedureAddress, GetProcedureAddress method [Media Foundation], GetProcedureAddress method [Media Foundation],IMFSignedLibrary interface, IMFSignedLibrary interface [Media Foundation],GetProcedureAddress method, IMFSignedLibrary.GetProcedureAddress, IMFSignedLibrary::GetProcedureAddress, mf.imfsignedlibrary_getprocedureaddress, mfidl/IMFSignedLibrary::GetProcedureAddress
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFSignedLibrary::GetProcedureAddress
 - mfidl/IMFSignedLibrary::GetProcedureAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSignedLibrary.GetProcedureAddress
---

# IMFSignedLibrary::GetProcedureAddress


## -description

Gets the procedure address of the specified function in the signed library.

## -parameters

### -param name

The entry point name in the DLL that specifies the function.

### -param address

Receives the address of the entry point.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -remarks

See  <a href="/windows/desktop/api/mfidl/nf-mfidl-mfloadsignedlibrary">MFLoadSignedLibrary</a> for an example of how to create an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary">IMFSignedLibrary</a> object and call the <b>GetProcedureAddress</b> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary">IMFSignedLibrary</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfloadsignedlibrary">MFLoadSignedLibrary</a>