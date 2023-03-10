---
UID: NF:wcmconfig.ITargetInfo.GetProperty
title: ITargetInfo::GetProperty (wcmconfig.h)
description: Gets a property value for the offline installation location.
helpviewer_keywords: ["GetProperty","GetProperty method [SMI]","GetProperty method [SMI]","ITargetInfo interface","ITargetInfo interface [SMI]","GetProperty method","ITargetInfo.GetProperty","ITargetInfo::GetProperty","smi.itargetinfo_getproperty","wcmconfig/ITargetInfo::GetProperty"]
old-location: smi\itargetinfo_getproperty.htm
tech.root: SMI
ms.assetid: f4366d23-e2dd-4561-af79-870212631ebf
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [SMI], GetProperty method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],GetProperty method, ITargetInfo.GetProperty, ITargetInfo::GetProperty, smi.itargetinfo_getproperty, wcmconfig/ITargetInfo::GetProperty
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITargetInfo::GetProperty
 - wcmconfig/ITargetInfo::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.GetProperty
---

# ITargetInfo::GetProperty


## -description

Gets a property value for the offline installation location.

## -parameters

### -param Offline [in]

<b>True</b> if the installation location is offline.

### -param Property [in]

The name of the property.

### -param Value [out]

The value of the property.

## -returns

This method can return one of these values.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the requested property does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there are insufficient resources to return information to the user.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>