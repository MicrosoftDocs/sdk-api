---
UID: NF:segment.IMSVidVMR9.SetAllocator
title: IMSVidVMR9::SetAllocator (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidVMR9 interface [Microsoft TV Technologies]","SetAllocator method","IMSVidVMR9.SetAllocator","IMSVidVMR9::SetAllocator","IMSVidVMR9SetAllocator","SetAllocator","SetAllocator method [Microsoft TV Technologies]","SetAllocator method [Microsoft TV Technologies]","IMSVidVMR9 interface","mstv.imsvidvmr9_setallocator","segment/IMSVidVMR9::SetAllocator"]
old-location: mstv\imsvidvmr9_setallocator.htm
tech.root: mstv
ms.assetid: f654adac-12b6-47c7-99d4-0612b1532df4
ms.date: 12/05/2018
ms.keywords: IMSVidVMR9 interface [Microsoft TV Technologies],SetAllocator method, IMSVidVMR9.SetAllocator, IMSVidVMR9::SetAllocator, IMSVidVMR9SetAllocator, SetAllocator, SetAllocator method [Microsoft TV Technologies], SetAllocator method [Microsoft TV Technologies],IMSVidVMR9 interface, mstv.imsvidvmr9_setallocator, segment/IMSVidVMR9::SetAllocator
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
 - IMSVidVMR9::SetAllocator
 - segment/IMSVidVMR9::SetAllocator
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
 - IMSVidVMR9.SetAllocator
---

# IMSVidVMR9::SetAllocator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>SetAllocator</b> method sets a custom allocator-presenter for the VMR-9.

## -parameters

### -param AllocPresent [in]

Pointer to the <b>IUnknown</b> interface of the allocator-presenter. This object must expose the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9</a> interface. To use the VMR-9 filter's default allocator-presenter, set this parameter to <b>NULL</b>.

### -param ID [in]

Application-defined identifier for the allocator-presenter.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvmr9">IMSVidVMR9 Interface</a>