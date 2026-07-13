---
UID: NF:segment.IMSVidVMR9.get_Allocator
title: IMSVidVMR9::get_Allocator (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidVMR9 interface [Microsoft TV Technologies]","get_Allocator method","IMSVidVMR9.get_Allocator","IMSVidVMR9::get_Allocator","IMSVidVMR9get_Allocator","get_Allocator","get_Allocator method [Microsoft TV Technologies]","get_Allocator method [Microsoft TV Technologies]","IMSVidVMR9 interface","mstv.imsvidvmr9_get_allocator","segment/IMSVidVMR9::get_Allocator"]
old-location: mstv\imsvidvmr9_get_allocator.htm
tech.root: mstv
ms.assetid: bd19c85b-21dc-410a-9fa1-99e1f1d8be30
ms.date: 12/05/2018
ms.keywords: IMSVidVMR9 interface [Microsoft TV Technologies],get_Allocator method, IMSVidVMR9.get_Allocator, IMSVidVMR9::get_Allocator, IMSVidVMR9get_Allocator, get_Allocator, get_Allocator method [Microsoft TV Technologies], get_Allocator method [Microsoft TV Technologies],IMSVidVMR9 interface, mstv.imsvidvmr9_get_allocator, segment/IMSVidVMR9::get_Allocator
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidVMR9::get_Allocator
 - segment/IMSVidVMR9::get_Allocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVMR9.get_Allocator
---

# IMSVidVMR9::get_Allocator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_Allocator</b> method retrieves the application's custom allocator-presenter.

## -parameters

### -param AllocPresent [out]

Receives a pointer to the <b>IUnknown</b> interface of the allocator-presenter. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The application did not set a custom allocator-presenter.

</td>
</tr>
</table>

## -remarks

To set a custom allocator-presenter, call <a href="/windows/desktop/api/segment/nf-segment-imsvidvmr9-setallocator">IMSVidVMR9::SetAllocator</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvmr9">IMSVidVMR9 Interface</a>