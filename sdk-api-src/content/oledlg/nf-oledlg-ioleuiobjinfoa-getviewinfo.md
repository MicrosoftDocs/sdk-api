---
UID: NF:oledlg.IOleUIObjInfoA.GetViewInfo
title: IOleUIObjInfoA::GetViewInfo (oledlg.h)
description: Gets the view information associated with the object. (ANSI)
helpviewer_keywords: ["GetViewInfo","GetViewInfo method [COM]","GetViewInfo method [COM]","IOleUIObjInfo interface","GetViewInfo method [COM]","IOleUIObjInfoA interface","GetViewInfo method [COM]","IOleUIObjInfoW interface","IOleUIObjInfo interface [COM]","GetViewInfo method","IOleUIObjInfo::GetViewInfo","IOleUIObjInfoA interface [COM]","GetViewInfo method","IOleUIObjInfoA.GetViewInfo","IOleUIObjInfoA::GetViewInfo","IOleUIObjInfoW interface [COM]","GetViewInfo method","IOleUIObjInfoW::GetViewInfo","_ole_IOleUIObjInfo_GetViewInfo","com.ioleuiobjinfo_getviewinfo","oledlg/IOleUIObjInfo::GetViewInfo","oledlg/IOleUIObjInfoA::GetViewInfo","oledlg/IOleUIObjInfoW::GetViewInfo"]
old-location: com\ioleuiobjinfo_getviewinfo.htm
tech.root: com
ms.assetid: 8e9774b6-1264-48d4-b5fb-c43b67e29f6e
ms.date: 12/05/2018
ms.keywords: GetViewInfo, GetViewInfo method [COM], GetViewInfo method [COM],IOleUIObjInfo interface, GetViewInfo method [COM],IOleUIObjInfoA interface, GetViewInfo method [COM],IOleUIObjInfoW interface, IOleUIObjInfo interface [COM],GetViewInfo method, IOleUIObjInfo::GetViewInfo, IOleUIObjInfoA interface [COM],GetViewInfo method, IOleUIObjInfoA.GetViewInfo, IOleUIObjInfoA::GetViewInfo, IOleUIObjInfoW interface [COM],GetViewInfo method, IOleUIObjInfoW::GetViewInfo, _ole_IOleUIObjInfo_GetViewInfo, com.ioleuiobjinfo_getviewinfo, oledlg/IOleUIObjInfo::GetViewInfo, oledlg/IOleUIObjInfoA::GetViewInfo, oledlg/IOleUIObjInfoW::GetViewInfo
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IOleUIObjInfoA::GetViewInfo
 - oledlg/IOleUIObjInfoA::GetViewInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleDlg.h
api_name:
 - IOleUIObjInfo.GetViewInfo
 - IOleUIObjInfoW.GetViewInfo
 - IOleUIObjInfoA.GetViewInfo
---

# IOleUIObjInfoA::GetViewInfo


## -description

Gets the view information associated with the object.

## -parameters

### -param dwObject [in]

Unique  identifier for the object.

### -param phMetaPict [in, optional]

Pointer to the object's current icon. This parameter can be <b>NULL</b>, indicating that the caller is not interested in the object's current presentation.

### -param pdvAspect [in, optional]

Pointer to the object's current aspect. This parameter can be <b>NULL</b>, indicating that the caller is not interested in the object's current aspect, for example, DVASPECT_ICONIC or DVASPECT_CONTENT.

### -param pnCurrentScale [in, optional]

Pointer to the object's current scale. This parameter can be <b>NULL</b>, indicating that the caller is not interested in the current scaling factor applied to the object in the container's view.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Insufficient access permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You must fill in the object's current icon, aspect, and scale.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuiobjinfoa">IOleUIObjInfo</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiviewpropsa">OLEUIVIEWPROPS</a>
