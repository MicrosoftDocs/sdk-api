---
UID: NF:qmgr.IBackgroundCopyGroup.SetProp
title: IBackgroundCopyGroup::SetProp (qmgr.h)
description: Use the SetProp method to set the property value for a group property.
helpviewer_keywords: ["IBackgroundCopyGroup interface [BITS]","SetProp method","IBackgroundCopyGroup.SetProp","IBackgroundCopyGroup::SetProp","SetProp","SetProp method [BITS]","SetProp method [BITS]","IBackgroundCopyGroup interface","bits.ibackgroundcopygroup_setprop","qmgr/IBackgroundCopyGroup::SetProp"]
old-location: bits\ibackgroundcopygroup_setprop.htm
tech.root: Bits
ms.assetid: 057a1004-fbe6-4c90-84c0-4e5b55539ce9
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],SetProp method, IBackgroundCopyGroup.SetProp, IBackgroundCopyGroup::SetProp, SetProp, SetProp method [BITS], SetProp method [BITS],IBackgroundCopyGroup interface, bits.ibackgroundcopygroup_setprop, qmgr/IBackgroundCopyGroup::SetProp
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
 - IBackgroundCopyGroup::SetProp
 - qmgr/IBackgroundCopyGroup::SetProp
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
 - IBackgroundCopyGroup.SetProp
---

# IBackgroundCopyGroup::SetProp


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>SetProp</b> method to set the property value for a group property.

## -parameters

### -param propID [in]

Identifies the property to set. For a list of properties, see the <a href="/windows/desktop/api/qmgr/ne-qmgr-groupprop">GROUPPROP</a> enumeration.

### -param pvarVal [in]

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
Successfully set the property.

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