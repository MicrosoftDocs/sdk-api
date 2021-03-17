---
UID: NF:strmif.IGetCapabilitiesKey.GetCapabilitiesKey
title: IGetCapabilitiesKey::GetCapabilitiesKey (strmif.h)
description: The GetCapabilitiesKey method gets a registry key that contains capability information for the codec.
helpviewer_keywords: ["GetCapabilitiesKey","GetCapabilitiesKey method [DirectShow]","GetCapabilitiesKey method [DirectShow]","IGetCapabilitiesKey interface","IGetCapabilitiesKey interface [DirectShow]","GetCapabilitiesKey method","IGetCapabilitiesKey.GetCapabilitiesKey","IGetCapabilitiesKey::GetCapabilitiesKey","IGetCapabilitiesKeyGetCapabiltitiesKey","dshow.igetcapabilitieskey_getcapabilitieskey","strmif/IGetCapabilitiesKey::GetCapabilitiesKey"]
old-location: dshow\igetcapabilitieskey_getcapabilitieskey.htm
tech.root: dshow
ms.assetid: 02c3edfe-9ce1-4d9f-bdd1-79e818b43800
ms.date: 12/05/2018
ms.keywords: GetCapabilitiesKey, GetCapabilitiesKey method [DirectShow], GetCapabilitiesKey method [DirectShow],IGetCapabilitiesKey interface, IGetCapabilitiesKey interface [DirectShow],GetCapabilitiesKey method, IGetCapabilitiesKey.GetCapabilitiesKey, IGetCapabilitiesKey::GetCapabilitiesKey, IGetCapabilitiesKeyGetCapabiltitiesKey, dshow.igetcapabilitieskey_getcapabilitieskey, strmif/IGetCapabilitiesKey::GetCapabilitiesKey
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetCapabilitiesKey::GetCapabilitiesKey
 - strmif/IGetCapabilitiesKey::GetCapabilitiesKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGetCapabilitiesKey.GetCapabilitiesKey
---

# IGetCapabilitiesKey::GetCapabilitiesKey


## -description

The <b>GetCapabilitiesKey</b> method gets a registry key that contains capability information for the codec.

## -parameters

### -param pHKey [out]

Receives a handle to the registry key. The caller must close the handle by calling <b>RegCloseKey</b>.

## -returns

This method can return one of these values.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
There is no capabilities key for this codec.

</td>
</tr>
</table>

## -remarks

To enumerate the values for the returned key, call <b>RegEnumValue</b>.

## -see-also

<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igetcapabilitieskey">IGetCapabilitiesKey</a>