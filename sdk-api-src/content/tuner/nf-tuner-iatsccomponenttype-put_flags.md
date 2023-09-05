---
UID: NF:tuner.IATSCComponentType.put_Flags
title: IATSCComponentType::put_Flags (tuner.h)
description: The put_Flags method specifies whether an audio component is in AC-3 format.
helpviewer_keywords: ["IATSCComponentType interface [Microsoft TV Technologies]","put_Flags method","IATSCComponentType.put_Flags","IATSCComponentType::put_Flags","IATSCComponentTypeput_Flags","mstv.iatsccomponenttype_put_flags","put_Flags","put_Flags method [Microsoft TV Technologies]","put_Flags method [Microsoft TV Technologies]","IATSCComponentType interface","tuner/IATSCComponentType::put_Flags"]
old-location: mstv\iatsccomponenttype_put_flags.htm
tech.root: mstv
ms.assetid: e2959a4c-70a8-43a4-8bc5-4bfc965e8085
ms.date: 12/05/2018
ms.keywords: IATSCComponentType interface [Microsoft TV Technologies],put_Flags method, IATSCComponentType.put_Flags, IATSCComponentType::put_Flags, IATSCComponentTypeput_Flags, mstv.iatsccomponenttype_put_flags, put_Flags, put_Flags method [Microsoft TV Technologies], put_Flags method [Microsoft TV Technologies],IATSCComponentType interface, tuner/IATSCComponentType::put_Flags
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IATSCComponentType::put_Flags
 - tuner/IATSCComponentType::put_Flags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IATSCComponentType.put_Flags
---

# IATSCComponentType::put_Flags


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Flags</b> method specifies whether an audio component is in AC-3 format.

## -parameters

### -param flags [in]

Specifies one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>The component does not contain AC-3 audio</td>
</tr>
<tr>
<td>ATSCCT_AC3</td>
<td>The component contains AC-3 audio</td>
</tr>
</table>
 

See <a href="/previous-versions/windows/desktop/mstv/atsccomponenttypeflags">ATSCComponentTypeFlags Enumeration</a>.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsccomponenttype">IATSCComponentType Interface</a>