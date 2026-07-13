---
UID: NF:oledlg.IOleUIObjInfoW.GetConvertInfo
title: IOleUIObjInfoW::GetConvertInfo (oledlg.h)
description: Gets the conversion information associated with the specified object. (Unicode)
helpviewer_keywords: ["GetConvertInfo","GetConvertInfo method [COM]","GetConvertInfo method [COM]","IOleUIObjInfo interface","GetConvertInfo method [COM]","IOleUIObjInfoA interface","GetConvertInfo method [COM]","IOleUIObjInfoW interface","IOleUIObjInfo interface [COM]","GetConvertInfo method","IOleUIObjInfo::GetConvertInfo","IOleUIObjInfoA interface [COM]","GetConvertInfo method","IOleUIObjInfoA::GetConvertInfo","IOleUIObjInfoW interface [COM]","GetConvertInfo method","IOleUIObjInfoW.GetConvertInfo","IOleUIObjInfoW::GetConvertInfo","_ole_IOleUIObjInfo_GetConvertInfo","com.ioleuiobjinfo_getconvertinfo","oledlg/IOleUIObjInfo::GetConvertInfo","oledlg/IOleUIObjInfoA::GetConvertInfo","oledlg/IOleUIObjInfoW::GetConvertInfo"]
old-location: com\ioleuiobjinfo_getconvertinfo.htm
tech.root: com
ms.assetid: 45416493-7f0b-4bef-b785-513d4f404541
ms.date: 12/05/2018
ms.keywords: GetConvertInfo, GetConvertInfo method [COM], GetConvertInfo method [COM],IOleUIObjInfo interface, GetConvertInfo method [COM],IOleUIObjInfoA interface, GetConvertInfo method [COM],IOleUIObjInfoW interface, IOleUIObjInfo interface [COM],GetConvertInfo method, IOleUIObjInfo::GetConvertInfo, IOleUIObjInfoA interface [COM],GetConvertInfo method, IOleUIObjInfoA::GetConvertInfo, IOleUIObjInfoW interface [COM],GetConvertInfo method, IOleUIObjInfoW.GetConvertInfo, IOleUIObjInfoW::GetConvertInfo, _ole_IOleUIObjInfo_GetConvertInfo, com.ioleuiobjinfo_getconvertinfo, oledlg/IOleUIObjInfo::GetConvertInfo, oledlg/IOleUIObjInfoA::GetConvertInfo, oledlg/IOleUIObjInfoW::GetConvertInfo
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
 - IOleUIObjInfoW::GetConvertInfo
 - oledlg/IOleUIObjInfoW::GetConvertInfo
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
 - IOleUIObjInfo.GetConvertInfo
 - IOleUIObjInfoW.GetConvertInfo
 - IOleUIObjInfoA.GetConvertInfo
---

# IOleUIObjInfoW::GetConvertInfo


## -description

Gets the conversion information associated with the specified object.

## -parameters

### -param dwObject [in]

Unique identifier for the object.

### -param lpClassID [out]

Pointer to the location to return the object's CLSID.

### -param lpwFormat [out]

Pointer to the clipboard format of the object.

### -param lpConvertDefaultClassID [out]

Pointer to the default class, selected from the UI, to convert the object to.

### -param lplpClsidExclude [out]

Address of a pointer variable that receives a pointer to an array of CLSIDs that should be excluded from the user interface for this object. If <i>lpcClsidExclude</i> is zero, then <i>lpClsidExclude</i> is set to <b>NULL</b>.

### -param lpcClsidExclude [out]

Address of an output variable that receives the number of CLSIDs in <i>lplpClsidExclude</i>. This parameter may be zero.

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
You must fill in the CLSID of the object at a minimum. <i>lpwFormat</i> may be left at zero if the format of the storage is unknown.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuiobjinfoa">IOleUIObjInfo</a>
