---
UID: NF:qmgr.IBackgroundCopyGroup.GetProp
title: IBackgroundCopyGroup::GetProp (qmgr.h)
description: Use the GetProp method to retrieve a property value from the group.
helpviewer_keywords: ["GetProp","GetProp method [BITS]","GetProp method [BITS]","IBackgroundCopyGroup interface","IBackgroundCopyGroup interface [BITS]","GetProp method","IBackgroundCopyGroup.GetProp","IBackgroundCopyGroup::GetProp","bits.ibackgroundcopygroup_getprop","qmgr/IBackgroundCopyGroup::GetProp"]
old-location: bits\ibackgroundcopygroup_getprop.htm
tech.root: Bits
ms.assetid: c27debdf-22eb-417e-b870-2891167f4498
ms.date: 12/05/2018
ms.keywords: GetProp, GetProp method [BITS], GetProp method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],GetProp method, IBackgroundCopyGroup.GetProp, IBackgroundCopyGroup::GetProp, bits.ibackgroundcopygroup_getprop, qmgr/IBackgroundCopyGroup::GetProp
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyGroup::GetProp
 - qmgr/IBackgroundCopyGroup::GetProp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.GetProp
---

# IBackgroundCopyGroup::GetProp


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetProp</b> method to retrieve a property value from the group.

## -parameters

### -param propID [in]

Identifies the property to retrieve. For a list of properties, see the <a href="/windows/desktop/api/qmgr/ne-qmgr-groupprop">GROUPPROP</a> enumeration.

### -param pvarVal [out]

Property value.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Successfully retrieved the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
You specified a property that is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
You specified a variant type that is not compatible with the property.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>