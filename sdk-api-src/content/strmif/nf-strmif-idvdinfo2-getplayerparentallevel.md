---
UID: NF:strmif.IDvdInfo2.GetPlayerParentalLevel
title: IDvdInfo2::GetPlayerParentalLevel (strmif.h)
description: The GetPlayerParentalLevel method retrieves the current parental level and ISO 3166 country/region code settings for the DVD Navigator.
helpviewer_keywords: ["GetPlayerParentalLevel","GetPlayerParentalLevel method [DirectShow]","GetPlayerParentalLevel method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetPlayerParentalLevel method","IDvdInfo2.GetPlayerParentalLevel","IDvdInfo2::GetPlayerParentalLevel","IDvdInfo2GetPlayerParentalLevel","dshow.idvdinfo2_getplayerparentallevel","strmif/IDvdInfo2::GetPlayerParentalLevel"]
old-location: dshow\idvdinfo2_getplayerparentallevel.htm
tech.root: dshow
ms.assetid: 7ae9b79a-1a2e-4679-9ead-6892491a1af3
ms.date: 12/05/2018
ms.keywords: GetPlayerParentalLevel, GetPlayerParentalLevel method [DirectShow], GetPlayerParentalLevel method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetPlayerParentalLevel method, IDvdInfo2.GetPlayerParentalLevel, IDvdInfo2::GetPlayerParentalLevel, IDvdInfo2GetPlayerParentalLevel, dshow.idvdinfo2_getplayerparentallevel, strmif/IDvdInfo2::GetPlayerParentalLevel
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo2::GetPlayerParentalLevel
 - strmif/IDvdInfo2::GetPlayerParentalLevel
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
 - IDvdInfo2.GetPlayerParentalLevel
---

# IDvdInfo2::GetPlayerParentalLevel


## -description

The <code>GetPlayerParentalLevel</code> method retrieves the current parental level and ISO 3166 country/region code settings for the DVD Navigator.

## -parameters

### -param pulParentalLevel [out]

Receives a value indicating the current parental level. Valid parental levels are 1 through 8 if parental management is enabled, 0xFFFFFFFF if parental management is disabled.

### -param pbCountryCode [out]

Address of a two-byte array that receives the current country/region code (ISO 3166 Alpha-2 Code).

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

</td>
</tr>
</table>

## -remarks

Parental management is disabled by default in the DVD Navigator. This method is demonstrated in the DVDSample application in <b>CDvdCore::GetParentalLevel</b>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/ec-dvd-parental-level-change">EC_DVD_PARENTAL_LEVEL_CHANGE</a>



<a href="/windows/desktop/DirectShow/enforcing-parental-management-levels">Enforcing Parental Management Levels</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>