---
UID: NF:oledlg.IOleUIObjInfoA.SetViewInfo
title: IOleUIObjInfoA::SetViewInfo (oledlg.h)
description: Sets the view information associated with the object. (ANSI)
helpviewer_keywords: ["IOleUIObjInfo interface [COM]","SetViewInfo method","IOleUIObjInfo::SetViewInfo","IOleUIObjInfoA interface [COM]","SetViewInfo method","IOleUIObjInfoA.SetViewInfo","IOleUIObjInfoA::SetViewInfo","IOleUIObjInfoW interface [COM]","SetViewInfo method","IOleUIObjInfoW::SetViewInfo","SetViewInfo","SetViewInfo method [COM]","SetViewInfo method [COM]","IOleUIObjInfo interface","SetViewInfo method [COM]","IOleUIObjInfoA interface","SetViewInfo method [COM]","IOleUIObjInfoW interface","_ole_IOleUIObjInfo_SetViewInfo","com.ioleuiobjinfo_setviewinfo","oledlg/IOleUIObjInfo::SetViewInfo","oledlg/IOleUIObjInfoA::SetViewInfo","oledlg/IOleUIObjInfoW::SetViewInfo"]
old-location: com\ioleuiobjinfo_setviewinfo.htm
tech.root: com
ms.assetid: 83d88f33-448f-4b8f-9c82-b6aaa4e8ff4a
ms.date: 12/05/2018
ms.keywords: IOleUIObjInfo interface [COM],SetViewInfo method, IOleUIObjInfo::SetViewInfo, IOleUIObjInfoA interface [COM],SetViewInfo method, IOleUIObjInfoA.SetViewInfo, IOleUIObjInfoA::SetViewInfo, IOleUIObjInfoW interface [COM],SetViewInfo method, IOleUIObjInfoW::SetViewInfo, SetViewInfo, SetViewInfo method [COM], SetViewInfo method [COM],IOleUIObjInfo interface, SetViewInfo method [COM],IOleUIObjInfoA interface, SetViewInfo method [COM],IOleUIObjInfoW interface, _ole_IOleUIObjInfo_SetViewInfo, com.ioleuiobjinfo_setviewinfo, oledlg/IOleUIObjInfo::SetViewInfo, oledlg/IOleUIObjInfoA::SetViewInfo, oledlg/IOleUIObjInfoW::SetViewInfo
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
 - IOleUIObjInfoA::SetViewInfo
 - oledlg/IOleUIObjInfoA::SetViewInfo
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
 - IOleUIObjInfo.SetViewInfo
 - IOleUIObjInfoW.SetViewInfo
 - IOleUIObjInfoA.SetViewInfo
---

# IOleUIObjInfoA::SetViewInfo


## -description

Sets the view information associated with the object.

## -parameters

### -param dwObject [in]

Unique identifier for the object.

### -param hMetaPict [in]

The new icon.

### -param dvAspect [in]

The new display aspect or view.

### -param nCurrentScale [in]

The new scale.

### -param bRelativeToOrig [in]

The new scale of the object, relative to the origin. This value is <b>TRUE</b> if the scale should be relative to the original scale of the object. If <b>FALSE</b>, <i>nCurrentScale</i> applies to the object's current size.

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
The specified identifier is invalid.

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
You should apply the new attributes (icon, aspect, and scale) to the object. If <i>bRelativeToOrig</i> is set to <b>TRUE</b>, <i>nCurrentScale</i> (in percentage units) applies to the original size of the object before it was scaled. If <i>bRelativeToOrig</i> is <b>FALSE</b>, <i>nCurrentScale</i> applies to the object's current size.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuiobjinfoa">IOleUIObjInfo</a>
