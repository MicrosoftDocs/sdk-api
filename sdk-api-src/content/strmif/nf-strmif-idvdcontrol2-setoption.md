---
UID: NF:strmif.IDvdControl2.SetOption
title: IDvdControl2::SetOption (strmif.h)
author: windows-sdk-content
description: The SetOption method enables or disables an internal behavior flag on the DVD Navigator filter.
old-location: dshow\idvdcontrol2_setoption.htm
tech.root: DirectShow
ms.assetid: b3b28da8-b0cb-4d76-8184-93572e4b6d06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetOption method, IDvdControl2.SetOption, IDvdControl2::SetOption, IDvdControl2SetOption, SetOption, SetOption method [DirectShow], SetOption method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setoption, strmif/IDvdControl2::SetOption
ms.topic: method
f1_keywords: 
 - "strmif/IDvdControl2.SetOption"
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
 - IDvdControl2.SetOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::SetOption


## -description



The <b>SetOption</b> method enables or disables an internal behavior flag on the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter.




## -parameters




### -param flag [in]

Specifies which behavior to modify, as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-__midl___midl_itf_strmif_0000_0132_0003">DVD_OPTION_FLAG</a> enumeration type. 


### -param fState [in]

Specifies the new value of the option given in the <i>flag</i> parameter.

<div class="alert"><b>Note</b>  This parameter is a <b>BOOL</b> type, but some options treat this parameter as a numeric value, not a Boolean value. For details, see the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-__midl___midl_itf_strmif_0000_0132_0003">DVD_OPTION_FLAG</a> reference page.
          </div>
<div> </div>

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
Invalid flag.

</td>
</tr>
</table>
 




## -remarks



Call <b>SetOption</b> with the desired flags immediately after creating an instance of the DVD Navigator and whenever you want to change any behaviors.
      

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.
      

<table>
<tr>
<th>Annex J Command Name
            </th>
<th>Valid Domains
            </th>
</tr>
<tr>
<td>None</td>
<td>All</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

