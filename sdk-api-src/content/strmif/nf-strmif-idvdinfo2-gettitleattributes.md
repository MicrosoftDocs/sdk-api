---
UID: NF:strmif.IDvdInfo2.GetTitleAttributes
title: IDvdInfo2::GetTitleAttributes (strmif.h)
description: The GetTitleAttributes method retrieves attributes of all video, audio, and subpicture streams for the specified title and its menus.helpviewer_keywords: ["GetTitleAttributes","GetTitleAttributes method [DirectShow]","GetTitleAttributes method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetTitleAttributes method","IDvdInfo2.GetTitleAttributes","IDvdInfo2::GetTitleAttributes","IDvdInfo2GetTitleAttributes","dshow.idvdinfo2_gettitleattributes","strmif/IDvdInfo2::GetTitleAttributes"]
old-location: dshow\idvdinfo2_gettitleattributes.htm
tech.root: DirectShow
ms.assetid: 4e901e14-9e98-4ca5-ae37-7a4564b187ab
ms.date: 12/05/2018
ms.keywords: GetTitleAttributes, GetTitleAttributes method [DirectShow], GetTitleAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetTitleAttributes method, IDvdInfo2.GetTitleAttributes, IDvdInfo2::GetTitleAttributes, IDvdInfo2GetTitleAttributes, dshow.idvdinfo2_gettitleattributes, strmif/IDvdInfo2::GetTitleAttributes
f1_keywords:
- strmif/IDvdInfo2.GetTitleAttributes
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
- IDvdInfo2.GetTitleAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetTitleAttributes


## -description



The <code>GetTitleAttributes</code> method retrieves attributes of all video, audio, and subpicture streams for the specified title and its menus.




## -parameters




### -param ulTitle [in]

Variable of type ULONG, from 1 through 99, specifying the requested title number. Specify 0xFFFFFFFF for the current title.


### -param pMenu [out]

Pointer to a [DVD_MenuAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_menuattributes) structure that receives the attributes of the menu associated with the specified title.


### -param pTitle [out]

Pointer to a [DVD_TitleAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_titleattributes) structure that receives the attributes of the specified title.


## -returns



Returns one of the following <code>HRESULT</code> values.

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
The <i>nTitle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not in the title domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pMenu</i> or <i>pTitle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD Navigator is not initialized or some other internal error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

