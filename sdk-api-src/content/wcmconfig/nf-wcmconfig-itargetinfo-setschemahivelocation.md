---
UID: NF:wcmconfig.ITargetInfo.SetSchemaHiveLocation
title: ITargetInfo::SetSchemaHiveLocation (wcmconfig.h)
description: Sets the location of the schema hive.
helpviewer_keywords: ["ITargetInfo interface [SMI]","SetSchemaHiveLocation method","ITargetInfo.SetSchemaHiveLocation","ITargetInfo::SetSchemaHiveLocation","SetSchemaHiveLocation","SetSchemaHiveLocation method [SMI]","SetSchemaHiveLocation method [SMI]","ITargetInfo interface","smi.itargetinfo_setschemahivelocation","wcmconfig/ITargetInfo::SetSchemaHiveLocation"]
old-location: smi\itargetinfo_setschemahivelocation.htm
tech.root: SMI
ms.assetid: 223ce821-4f31-4673-95e2-ec9cf94d5726
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],SetSchemaHiveLocation method, ITargetInfo.SetSchemaHiveLocation, ITargetInfo::SetSchemaHiveLocation, SetSchemaHiveLocation, SetSchemaHiveLocation method [SMI], SetSchemaHiveLocation method [SMI],ITargetInfo interface, smi.itargetinfo_setschemahivelocation, wcmconfig/ITargetInfo::SetSchemaHiveLocation
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
 - ITargetInfo::SetSchemaHiveLocation
 - wcmconfig/ITargetInfo::SetSchemaHiveLocation
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
 - ITargetInfo.SetSchemaHiveLocation
---

# ITargetInfo::SetSchemaHiveLocation


## -description

Sets the location of the schema hive.

## -parameters

### -param pwzHiveDir [in]

A pointer to the location of the schema hive.

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
<dt><b> E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the system is low on resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the location <i>pwzHiveDir</i> is not a directory.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>