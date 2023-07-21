---
UID: NF:tuner.IATSCComponentType.get_Flags
title: IATSCComponentType::get_Flags (tuner.h)
description: The get_Flags method queries whether an audio component is in AC-3 format.
helpviewer_keywords: ["IATSCComponentType interface [Microsoft TV Technologies]","get_Flags method","IATSCComponentType.get_Flags","IATSCComponentType::get_Flags","IATSCComponentTypeget_Flags","get_Flags","get_Flags method [Microsoft TV Technologies]","get_Flags method [Microsoft TV Technologies]","IATSCComponentType interface","mstv.iatsccomponenttype_get_flags","tuner/IATSCComponentType::get_Flags"]
old-location: mstv\iatsccomponenttype_get_flags.htm
tech.root: mstv
ms.assetid: f89f59fd-31bf-48d6-9cb3-92504ba095a9
ms.date: 12/05/2018
ms.keywords: IATSCComponentType interface [Microsoft TV Technologies],get_Flags method, IATSCComponentType.get_Flags, IATSCComponentType::get_Flags, IATSCComponentTypeget_Flags, get_Flags, get_Flags method [Microsoft TV Technologies], get_Flags method [Microsoft TV Technologies],IATSCComponentType interface, mstv.iatsccomponenttype_get_flags, tuner/IATSCComponentType::get_Flags
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
 - IATSCComponentType::get_Flags
 - tuner/IATSCComponentType::get_Flags
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
 - IATSCComponentType.get_Flags
---

# IATSCComponentType::get_Flags


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Flags</b> method queries whether an audio component is in AC-3 format.

## -parameters

### -param Flags [out]

Receives one of the following values.

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