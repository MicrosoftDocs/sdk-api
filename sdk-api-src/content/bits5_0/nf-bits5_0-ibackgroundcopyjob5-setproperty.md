---
UID: NF:bits5_0.IBackgroundCopyJob5.SetProperty
title: IBackgroundCopyJob5::SetProperty (bits5_0.h)
description: A generic method for setting BITS job properties.
helpviewer_keywords: ["IBackgroundCopyJob5 interface [BITS]","SetProperty method","IBackgroundCopyJob5.SetProperty","IBackgroundCopyJob5::SetProperty","SetProperty","SetProperty method [BITS]","SetProperty method [BITS]","IBackgroundCopyJob5 interface","bits.ibackgroundcopyjob5_setproperty","bits5_0/IBackgroundCopyJob5::SetProperty"]
old-location: bits\ibackgroundcopyjob5_setproperty.htm
tech.root: Bits
ms.assetid: D5DB8A96-7417-4142-BA27-783314835CED
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob5 interface [BITS],SetProperty method, IBackgroundCopyJob5.SetProperty, IBackgroundCopyJob5::SetProperty, SetProperty, SetProperty method [BITS], SetProperty method [BITS],IBackgroundCopyJob5 interface, bits.ibackgroundcopyjob5_setproperty, bits5_0/IBackgroundCopyJob5::SetProperty
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
 - IBackgroundCopyJob5::SetProperty
 - bits5_0/IBackgroundCopyJob5::SetProperty
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
 - IBackgroundCopyJob5.SetProperty
---

# IBackgroundCopyJob5::SetProperty


## -description

A generic method for setting BITS job properties.

## -parameters

### -param PropertyId [in]

The ID of the property that is being set specified as a <a href="/windows/desktop/api/bits5_0/ne-bits5_0-bits_job_property_id">BITS_JOB_PROPERTY_ID</a> enum value.

### -param PropertyValue [in]

The value of the property that is being set. In order to hold a value whose type is appropriate to the property, this value is specified via the <a href="/windows/desktop/api/bits5_0/ns-bits5_0-bits_job_property_value">BITS_JOB_PROPERTY_VALUE</a> union that is composed of all the known property types.

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



<b>IBackgroundCopyJob5::GetProperty</b>