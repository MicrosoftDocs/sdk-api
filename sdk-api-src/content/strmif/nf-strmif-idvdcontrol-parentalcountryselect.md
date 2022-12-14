---
UID: NF:strmif.IDvdControl.ParentalCountrySelect
title: IDvdControl::ParentalCountrySelect (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the current country/region for controlling parental access levels.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","ParentalCountrySelect method","IDvdControl.ParentalCountrySelect","IDvdControl::ParentalCountrySelect","IDvdControlParentalCountrySelect","ParentalCountrySelect","ParentalCountrySelect method [DirectShow]","ParentalCountrySelect method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_parentalcountryselect","strmif/IDvdControl::ParentalCountrySelect"]
old-location: dshow\idvdcontrol_parentalcountryselect.htm
tech.root: dshow
ms.assetid: fc79ad9b-4044-4a33-83b4-f3033283058a
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],ParentalCountrySelect method, IDvdControl.ParentalCountrySelect, IDvdControl::ParentalCountrySelect, IDvdControlParentalCountrySelect, ParentalCountrySelect, ParentalCountrySelect method [DirectShow], ParentalCountrySelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_parentalcountryselect, strmif/IDvdControl::ParentalCountrySelect
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDvdControl::ParentalCountrySelect
 - strmif/IDvdControl::ParentalCountrySelect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.ParentalCountrySelect
---

# IDvdControl::ParentalCountrySelect


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the current country/region for controlling parental access levels.

## -parameters

### -param wCountry [in]

Value that specifies the current country/region according to the Alpha-2 Code defined in ISO3166. See Remarks.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

The ISO3166 2-letter country/region codes in the <i>wCountry</i> parameter must be supplied to this method as a WORD. The conversion is demonstrated for the United States (US) in the following line of code.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
WORD wCountry  =  ( WORD( 'U' ) &lt;&lt; 8 ) | 'S';
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-parentallevelselect">IDvdControl::ParentalLevelSelect</a>