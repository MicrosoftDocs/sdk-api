---
UID: NF:bits5_0.IBackgroundCopyJob5.GetProperty
title: IBackgroundCopyJob5::GetProperty (bits5_0.h)
description: A generic method for getting BITS job properties.
helpviewer_keywords: ["GetProperty","GetProperty method [BITS]","GetProperty method [BITS]","IBackgroundCopyJob5 interface","IBackgroundCopyJob5 interface [BITS]","GetProperty method","IBackgroundCopyJob5.GetProperty","IBackgroundCopyJob5::GetProperty","bits.ibackgroundcopyjob5_getproperty","bits5_0/IBackgroundCopyJob5::GetProperty"]
old-location: bits\ibackgroundcopyjob5_getproperty.htm
tech.root: Bits
ms.assetid: 567C21C7-C689-4A13-9DCA-D45766CB5150
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [BITS], GetProperty method [BITS],IBackgroundCopyJob5 interface, IBackgroundCopyJob5 interface [BITS],GetProperty method, IBackgroundCopyJob5.GetProperty, IBackgroundCopyJob5::GetProperty, bits.ibackgroundcopyjob5_getproperty, bits5_0/IBackgroundCopyJob5::GetProperty
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob5::GetProperty
 - bits5_0/IBackgroundCopyJob5::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJob5.GetProperty
---

# IBackgroundCopyJob5::GetProperty


## -description

A generic method for getting BITS job properties.

## -parameters

### -param PropertyId [in]

The ID of the property that is being obtained specified as a <a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_property_id">BITS_JOB_PROPERTY_ID</a> enum value.

### -param PropertyValue [out]

The property value returned as a BITS_JOB_PROPERTY_VALUE union.

## -returns

The method returns the following return values.

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
Success

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits5_0/nn-bits5_0-ibackgroundcopyjob5">IBackgroundCopyJob5</a>



<a href="/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty">IBackgroundCopyJob5::SetProperty</a>