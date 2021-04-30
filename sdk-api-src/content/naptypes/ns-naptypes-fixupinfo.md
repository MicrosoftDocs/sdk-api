---
UID: NS:naptypes.tagFixupInfo
title: FixupInfo (naptypes.h)
description: Contains fix-up information for the Sysytem Health Agent (SHA).
helpviewer_keywords: ["FixupInfo","FixupInfo structure [NAP]","nap.fixupinfo_struct","naptypes/FixupInfo"]
old-location: nap\fixupinfo_struct.htm
tech.root: NAP
ms.assetid: 8f91534e-3281-4d5a-9af7-5f08eb0243f0
ms.date: 12/05/2018
ms.keywords: FixupInfo, FixupInfo structure [NAP], nap.fixupinfo_struct, naptypes/FixupInfo
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FixupInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFixupInfo
 - naptypes/tagFixupInfo
 - FixupInfo
 - naptypes/FixupInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - FixupInfo
---

# FixupInfo structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FixupInfo</b> structure contains fix-up information for the Sysytem Health Agent (SHA).

## -struct-fields

### -field state

A <a href="/windows/desktop/api/naptypes/ne-naptypes-fixupstate">FixupState</a> value that defines the fix-up state of the SHA.

### -field percentage

A <a href="/windows/desktop/NAP/nap-datatypes">Percentage</a> data type that contains the percentage of remediation that is complete. This member is a nonzero value between 0 (zero) and 100 when <b>state</b> is equal to <a href="/windows/desktop/api/naptypes/ne-naptypes-fixupstate">FixupStateInProgress</a>; otherwise, it is 0 (zero).

<div class="alert"><b>Note</b>  If the SHA does not support percentages, this value is either 0, which indicates the SHA update has not started; or 101, which indicates the SHA is in the process of updating.</div>
<div> </div>

### -field resultCodes

A <a href="/windows/desktop/api/naptypes/ns-naptypes-resultcodes">ResultCodes</a> structure that contains the SHA defined HRESULT values returned to the NAP Agent in a call to <a href="/windows/desktop/NAP/inapsystemhealthagentcallback-getfixupinfo-method">GetFixupInfo</a>.

### -field fixupMsgId

A <a href="/windows/desktop/NAP/nap-datatypes">MessageID</a> value that contains the SHA defined resource ID of a fix-up status structure.

## -remarks

If your SHA remediation process supports the reporting of percentage values during update, <b>percentage</b> is used to communicate the current progress as an integer percentage value. When the remediation update is complete, <b>percentage</b> must be set to 100, and <b>state</b> must be set to <b>fixupStateSuccess</b>. If remediation is not complete, <b>percentage</b> must be set to a value between 0 and 99, inclusive, and <b>state</b> must be set to <b>fixupStateInProgress</b>.

If your remediation process does not support the reporting of percentage values, then as long as <b>state</b> is set to <b>fixupStateInProgress</b>, <b>percentage</b> must be set to a value of 101, which indicates the remediation process is in a general "updating" state but the amount of completion is unknown. When remediation completes, <b>state</b> must be set to <b>fixupStateSuccess</b> and <b>percentage</b> must be set to 100.

If the SHA cannot update the fix-up information, then <b>state</b> must be set to <b>fixupStateCouldNotUpdate</b>.

## -see-also

<a href="/windows/desktop/api/naptypes/ne-naptypes-fixupstate">FixupState</a>



<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>



<a href="/windows/desktop/api/naptypes/ns-naptypes-resultcodes">ResultCodes</a>