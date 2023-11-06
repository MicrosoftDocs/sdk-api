---
UID: NF:msvidctl.IMSVidCtl.get_State
title: IMSVidCtl::get_State (msvidctl.h)
description: The get_State method retrieves the state of the filter graph.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_State method","IMSVidCtl.get_State","IMSVidCtl::get_State","IMSVidCtlget_State","get_State","get_State method [Microsoft TV Technologies]","get_State method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_state","msvidctl/IMSVidCtl::get_State"]
old-location: mstv\imsvidctl_get_state.htm
tech.root: mstv
ms.assetid: 45f35832-709c-4f78-9e1a-a6ad489fc81f
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_State method, IMSVidCtl.get_State, IMSVidCtl::get_State, IMSVidCtlget_State, get_State, get_State method [Microsoft TV Technologies], get_State method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_state, msvidctl/IMSVidCtl::get_State
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - IMSVidCtl::get_State
 - msvidctl/IMSVidCtl::get_State
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_State
---

# IMSVidCtl::get_State


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_State</b> method retrieves the state of the filter graph.

## -parameters

### -param lState [out]

Receives a member of the <a href="/previous-versions/windows/desktop/api/msvidctl/ne-msvidctl-msvidctlstatelist">MSVidCtlStateList</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>