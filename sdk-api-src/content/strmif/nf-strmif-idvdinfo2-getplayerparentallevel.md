---
UID: NF:strmif.IDvdInfo2.GetPlayerParentalLevel
title: IDvdInfo2::GetPlayerParentalLevel (strmif.h)
author: windows-sdk-content
description: The GetPlayerParentalLevel method retrieves the current parental level and ISO 3166 country/region code settings for the DVD Navigator.
old-location: dshow\idvdinfo2_getplayerparentallevel.htm
tech.root: DirectShow
ms.assetid: 7ae9b79a-1a2e-4679-9ead-6892491a1af3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPlayerParentalLevel, GetPlayerParentalLevel method [DirectShow], GetPlayerParentalLevel method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetPlayerParentalLevel method, IDvdInfo2.GetPlayerParentalLevel, IDvdInfo2::GetPlayerParentalLevel, IDvdInfo2GetPlayerParentalLevel, dshow.idvdinfo2_getplayerparentallevel, strmif/IDvdInfo2::GetPlayerParentalLevel
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/c6817e1a-f860-4ba2-9e0f-e195624230c5">EC_DVD_PARENTAL_LEVEL_CHANGE</a>



<a href="https://msdn.microsoft.com/ad996a03-e94e-4743-90a2-aa390984a231">Enforcing Parental Management Levels</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

