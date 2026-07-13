---
UID: NF:oledlg.IOleUILinkInfoW.GetLastUpdate
title: IOleUILinkInfoW::GetLastUpdate (oledlg.h)
description: Determines the last time the object was updated. (Unicode)
helpviewer_keywords: ["GetLastUpdate","GetLastUpdate method [COM]","GetLastUpdate method [COM]","IOleUILinkInfo interface","GetLastUpdate method [COM]","IOleUILinkInfoA interface","GetLastUpdate method [COM]","IOleUILinkInfow interface","IOleUILinkInfo interface [COM]","GetLastUpdate method","IOleUILinkInfo::GetLastUpdate","IOleUILinkInfoA","IOleUILinkInfoA interface [COM]","GetLastUpdate method","IOleUILinkInfoA::GetLastUpdate","IOleUILinkInfoW","IOleUILinkInfoW.GetLastUpdate","IOleUILinkInfoW::GetLastUpdate","IOleUILinkInfow interface [COM]","GetLastUpdate method","IOleUILinkInfow::GetLastUpdate","_ole_IOleUILinkInfo_GetLastUpdate","com.ioleuilinkinfo_getlastupdate","oledlg/IOleUILinkInfo::GetLastUpdate","oledlg/IOleUILinkInfoA::GetLastUpdate","oledlg/IOleUILinkInfow::GetLastUpdate"]
old-location: com\ioleuilinkinfo_getlastupdate.htm
tech.root: com
ms.assetid: 651dcfbc-577b-45a2-bf73-148a6f1c7030
ms.date: 12/05/2018
ms.keywords: GetLastUpdate, GetLastUpdate method [COM], GetLastUpdate method [COM],IOleUILinkInfo interface, GetLastUpdate method [COM],IOleUILinkInfoA interface, GetLastUpdate method [COM],IOleUILinkInfow interface, IOleUILinkInfo interface [COM],GetLastUpdate method, IOleUILinkInfo::GetLastUpdate, IOleUILinkInfoA, IOleUILinkInfoA interface [COM],GetLastUpdate method, IOleUILinkInfoA::GetLastUpdate, IOleUILinkInfoW, IOleUILinkInfoW.GetLastUpdate, IOleUILinkInfoW::GetLastUpdate, IOleUILinkInfow interface [COM],GetLastUpdate method, IOleUILinkInfow::GetLastUpdate, _ole_IOleUILinkInfo_GetLastUpdate, com.ioleuilinkinfo_getlastupdate, oledlg/IOleUILinkInfo::GetLastUpdate, oledlg/IOleUILinkInfoA::GetLastUpdate, oledlg/IOleUILinkInfow::GetLastUpdate
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
 - IOleUILinkInfoW::GetLastUpdate
 - oledlg/IOleUILinkInfoW::GetLastUpdate
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
 - IOleUILinkInfo.GetLastUpdate
 - IOleUILinkInfoA.GetLastUpdate
 - IOleUILinkInfow.GetLastUpdate
---

# IOleUILinkInfoW::GetLastUpdate


## -description

Determines the last time the object was updated.

## -parameters

### -param dwLink [in]

Container-defined unique identifier for a single link. Containers can use the pointer to the link's container site for this value.

### -param lpLastUpdate [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that indicates the time that the object was last updated.

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
If the time that the object was last updated is known, copy it to <i>lpLastUpdate</i>. If it is not known, then leave <i>lpLastUpdate</i> unchanged and Unknown will be displayed in the link page.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkinfoa">IOleUILinkInfo</a>
