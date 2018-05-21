---
UID: NF:strmif.IDvdControl2.SelectParentalCountry
title: IDvdControl2::SelectParentalCountry
author: windows-driver-content
description: The SelectParentalCountry method sets the country/region for interpreting parental access levels and setting default languages.
old-location: dshow\idvdcontrol2_selectparentalcountry.htm
old-project: DirectShow
ms.assetid: fb0b3fa9-c6e5-49a4-bec7-1e4e7d07ba46
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectParentalCountry method, IDvdControl2.SelectParentalCountry, IDvdControl2::SelectParentalCountry, IDvdControl2SelectParentalCountry, SelectParentalCountry, SelectParentalCountry method [DirectShow], SelectParentalCountry method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectparentalcountry, strmif/IDvdControl2::SelectParentalCountry
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdControl2.SelectParentalCountry
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::SelectParentalCountry


## -description



The <code>SelectParentalCountry</code> method sets the country/region for interpreting parental access levels and setting default languages.




## -parameters




### -param bCountry






#### - country_region [in]

Array of bytes that specifies the current country/region according to ISO 3166.


## -returns



Returns one of the following values.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter is not in a valid domain.

</td>
</tr>
</table>
 




## -remarks



The parental country/region determines the meaning of the eight generic parental levels as well as the default language for the soundtrack and menus. For details, see <a href="https://msdn.microsoft.com/ad996a03-e94e-4743-90a2-aa390984a231">Enforcing Parental Management Levels</a>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>
              Annex J Command Name
            </td>
<td>
              Valid Domains
            </td>
</tr>
<tr>
<td>Parental_Country_Select</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

