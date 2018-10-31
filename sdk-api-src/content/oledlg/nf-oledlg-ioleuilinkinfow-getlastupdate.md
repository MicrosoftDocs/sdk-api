---
UID: NF:oledlg.IOleUILinkInfoW.GetLastUpdate
title: IOleUILinkInfoW::GetLastUpdate
author: windows-sdk-content
description: Determines the last time the object was updated.
old-location: com\ioleuilinkinfo_getlastupdate.htm
tech.root: com
ms.assetid: 651dcfbc-577b-45a2-bf73-148a6f1c7030
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetLastUpdate, GetLastUpdate method [COM], GetLastUpdate method [COM],IOleUILinkInfo interface, GetLastUpdate method [COM],IOleUILinkInfoA interface, GetLastUpdate method [COM],IOleUILinkInfow interface, IOleUILinkInfo interface [COM],GetLastUpdate method, IOleUILinkInfo::GetLastUpdate, IOleUILinkInfoA, IOleUILinkInfoA interface [COM],GetLastUpdate method, IOleUILinkInfoA::GetLastUpdate, IOleUILinkInfoW, IOleUILinkInfoW.GetLastUpdate, IOleUILinkInfoW::GetLastUpdate, IOleUILinkInfow interface [COM],GetLastUpdate method, IOleUILinkInfow::GetLastUpdate, _ole_IOleUILinkInfo_GetLastUpdate, com.ioleuilinkinfo_getlastupdate, oledlg/IOleUILinkInfo::GetLastUpdate, oledlg/IOleUILinkInfoA::GetLastUpdate, oledlg/IOleUILinkInfow::GetLastUpdate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUILinkInfoW::GetLastUpdate


## -description


Determines the last time the object was updated.


## -parameters




### -param dwLink [in]

Container-defined unique identifier for a single link. Containers can use the pointer to the link's container site for this value.


### -param lpLastUpdate [out]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that indicates the time that the object was last updated.


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




<a href="https://msdn.microsoft.com/aadac00b-47bb-42eb-8458-b23867f6b975">IOleUILinkInfo</a>
 

 

