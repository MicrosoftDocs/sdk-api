---
UID: NF:richole.IRichEditOle.GetObject
title: IRichEditOle::GetObject (richole.h)
description: Retrieves information, stored in a REOBJECT structure, about an object in a rich edit control.
helpviewer_keywords: ["GetObject","GetObject method [Windows Controls]","GetObject method [Windows Controls]","IRichEditOle interface","IRichEditOle interface [Windows Controls]","GetObject method","IRichEditOle.GetObject","IRichEditOle::GetObject","REO_GETOBJ_ALL_INTERFACES","REO_GETOBJ_NO_INTERFACES","REO_GETOBJ_POLEOBJ","REO_GETOBJ_POLESITE","REO_GETOBJ_PSTG","_win32_IRichEditOle_GetObject","_win32_IRichEditOle_GetObject_cpp","controls.IRichEditOle_GetObject","controls._win32_IRichEditOle_GetObject","richole/IRichEditOle::GetObject"]
old-location: controls\IRichEditOle_GetObject.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolegetobject.htm
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Windows Controls], GetObject method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],GetObject method, IRichEditOle.GetObject, IRichEditOle::GetObject, REO_GETOBJ_ALL_INTERFACES, REO_GETOBJ_NO_INTERFACES, REO_GETOBJ_POLEOBJ, REO_GETOBJ_POLESITE, REO_GETOBJ_PSTG, _win32_IRichEditOle_GetObject, _win32_IRichEditOle_GetObject_cpp, controls.IRichEditOle_GetObject, controls._win32_IRichEditOle_GetObject, richole/IRichEditOle::GetObject
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditOle::GetObject
 - richole/IRichEditOle::GetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOle.GetObject
---

# IRichEditOle::GetObject


## -description

Retrieves information, stored in a <a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a> structure, about an object in a rich edit control.

## -parameters

### -param iob

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Zero-based index that specifies which object to return information about. If this parameter is <b>REO_IOB_USE_CP</b>, information about the object at the character position specified by the <a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a> structure is returned.

### -param lpreobject

Type: <b><a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a>*</b>

Structure that receives information about the object. The reference count of the interfaces returned in this structure has been incremented; it is the responsibility of the caller to use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method to decrement the count.

### -param dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Operation flags that specify which interfaces to return in the structure. The <i>dwFlags</i> parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_POLEOBJ"></a><a id="reo_getobj_poleobj"></a><dl>
<dt><b>REO_GETOBJ_POLEOBJ</b></dt>
</dl>
</td>
<td width="60%">
Get object interface.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_PSTG"></a><a id="reo_getobj_pstg"></a><dl>
<dt><b>REO_GETOBJ_PSTG</b></dt>
</dl>
</td>
<td width="60%">
Get storage interface.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_POLESITE"></a><a id="reo_getobj_polesite"></a><dl>
<dt><b>REO_GETOBJ_POLESITE</b></dt>
</dl>
</td>
<td width="60%">
Get site interface.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_NO_INTERFACES"></a><a id="reo_getobj_no_interfaces"></a><dl>
<dt><b>REO_GETOBJ_NO_INTERFACES</b></dt>
</dl>
</td>
<td width="60%">
Get no interfaces.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_ALL_INTERFACES"></a><a id="reo_getobj_all_interfaces"></a><dl>
<dt><b>REO_GETOBJ_ALL_INTERFACES</b></dt>
</dl>
</td>
<td width="60%">
Get all interfaces.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> if successful, or an error value otherwise. <b>E_INVALIDARG</b> is returned if no buffer for the <a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a> structure was given or if the <i>iob</i> value or character position is invalid.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>



<a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a>



<b>Reference</b>