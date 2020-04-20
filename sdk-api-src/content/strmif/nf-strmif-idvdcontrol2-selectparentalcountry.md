---
UID: NF:strmif.IDvdControl2.SelectParentalCountry
title: IDvdControl2::SelectParentalCountry (strmif.h)
description: The SelectParentalCountry method sets the country/region for interpreting parental access levels and setting default languages.helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectParentalCountry method","IDvdControl2.SelectParentalCountry","IDvdControl2::SelectParentalCountry","IDvdControl2SelectParentalCountry","SelectParentalCountry","SelectParentalCountry method [DirectShow]","SelectParentalCountry method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectparentalcountry","strmif/IDvdControl2::SelectParentalCountry"]
old-location: dshow\idvdcontrol2_selectparentalcountry.htm
tech.root: DirectShow
ms.assetid: fb0b3fa9-c6e5-49a4-bec7-1e4e7d07ba46
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectParentalCountry method, IDvdControl2.SelectParentalCountry, IDvdControl2::SelectParentalCountry, IDvdControl2SelectParentalCountry, SelectParentalCountry, SelectParentalCountry method [DirectShow], SelectParentalCountry method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectparentalcountry, strmif/IDvdControl2::SelectParentalCountry
f1_keywords:
- strmif/IDvdControl2.SelectParentalCountry
dev_langs:
- c++
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
- IDvdControl2.SelectParentalCountry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::SelectParentalCountry


## -description



The <code>SelectParentalCountry</code> method sets the country/region for interpreting parental access levels and setting default languages.




## -parameters




### -param bCountry [in]

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
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter is not in a valid domain.

</td>
</tr>
</table>
 




## -remarks



The parental country/region determines the meaning of the eight generic parental levels as well as the default language for the soundtrack and menus. For details, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/enforcing-parental-management-levels">Enforcing Parental Management Levels</a>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Parental_Country_Select</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

