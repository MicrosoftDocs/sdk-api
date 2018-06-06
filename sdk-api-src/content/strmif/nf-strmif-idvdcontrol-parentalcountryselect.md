---
UID: NF:strmif.IDvdControl.ParentalCountrySelect
title: IDvdControl::ParentalCountrySelect
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the current country/region for controlling parental access levels.
old-location: dshow\idvdcontrol_parentalcountryselect.htm
old-project: DirectShow
ms.assetid: fc79ad9b-4044-4a33-83b4-f3033283058a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IDvdControl interface [DirectShow],ParentalCountrySelect method, IDvdControl.ParentalCountrySelect, IDvdControl::ParentalCountrySelect, IDvdControlParentalCountrySelect, ParentalCountrySelect, ParentalCountrySelect method [DirectShow], ParentalCountrySelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_parentalcountryselect, strmif/IDvdControl::ParentalCountrySelect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.ParentalCountrySelect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::ParentalCountrySelect


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Sets the current country/region for controlling parental access levels.




## -parameters




### -param wCountry [in]

Value that specifies the current country/region according to the Alpha-2 Code defined in ISO3166. See Remarks.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

The ISO3166 2-letter country/region codes in the <i>wCountry</i> parameter must be supplied to this method as a WORD. The conversion is demonstrated for the United States (US) in the following line of code.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>



<a href="https://msdn.microsoft.com/ca572d89-b188-442d-884f-0cffa71c2892">IDvdControl::ParentalLevelSelect</a>
 

 

