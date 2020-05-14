---
UID: NF:medparam.IMediaParamInfo.GetSupportedTimeFormat
title: IMediaParamInfo::GetSupportedTimeFormat (medparam.h)
description: The GetSupportedTimeFormat method retrieves a supported time format.helpviewer_keywords: ["GetSupportedTimeFormat","GetSupportedTimeFormat method [DirectShow]","GetSupportedTimeFormat method [DirectShow]","IMediaParamInfo interface","IMediaParamInfo interface [DirectShow]","GetSupportedTimeFormat method","IMediaParamInfo.GetSupportedTimeFormat","IMediaParamInfo::GetSupportedTimeFormat","IMediaParamInfoGetSupportedTimeFormat","dshow.imediaparaminfo_getsupportedtimeformat","medparam/IMediaParamInfo::GetSupportedTimeFormat"]
old-location: dshow\imediaparaminfo_getsupportedtimeformat.htm
tech.root: DirectShow
ms.assetid: 04e4c9ea-4570-4fd0-986b-c835c692b73b
ms.date: 12/05/2018
ms.keywords: GetSupportedTimeFormat, GetSupportedTimeFormat method [DirectShow], GetSupportedTimeFormat method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetSupportedTimeFormat method, IMediaParamInfo.GetSupportedTimeFormat, IMediaParamInfo::GetSupportedTimeFormat, IMediaParamInfoGetSupportedTimeFormat, dshow.imediaparaminfo_getsupportedtimeformat, medparam/IMediaParamInfo::GetSupportedTimeFormat
f1_keywords:
- medparam/IMediaParamInfo.GetSupportedTimeFormat
dev_langs:
- c++
req.header: medparam.h
req.include-header: 
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dmoguids.lib
- Dmoguids.dll
api_name:
- IMediaParamInfo.GetSupportedTimeFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaParamInfo::GetSupportedTimeFormat


## -description



The <code>GetSupportedTimeFormat</code> method retrieves a supported time format.




## -parameters




### -param dwFormatIndex [in]

Index of the time format to retrieve.


### -param pguidTimeFormat [out]

Pointer to a variable that receives a time format GUID.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
</table>
 




## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getnumtimeformats">GetNumTimeFormats</a> method to retrieve the number of time formats that the object supports.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>
 

 

