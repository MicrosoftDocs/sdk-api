---
UID: NF:wcmconfig.ITargetInfo.GetSchemaHiveMountName
title: ITargetInfo::GetSchemaHiveMountName (wcmconfig.h)
description: Gets the name of the mount location of the schema hive.
helpviewer_keywords: ["GetSchemaHiveMountName","GetSchemaHiveMountName method [SMI]","GetSchemaHiveMountName method [SMI]","ITargetInfo interface","ITargetInfo interface [SMI]","GetSchemaHiveMountName method","ITargetInfo.GetSchemaHiveMountName","ITargetInfo::GetSchemaHiveMountName","smi.itargetinfo_getschemahivemountname","wcmconfig/ITargetInfo::GetSchemaHiveMountName"]
old-location: smi\itargetinfo_getschemahivemountname.htm
tech.root: SMI
ms.assetid: d63e3f49-bb7b-4ef6-a573-811b9bbdd9b0
ms.date: 12/05/2018
ms.keywords: GetSchemaHiveMountName, GetSchemaHiveMountName method [SMI], GetSchemaHiveMountName method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],GetSchemaHiveMountName method, ITargetInfo.GetSchemaHiveMountName, ITargetInfo::GetSchemaHiveMountName, smi.itargetinfo_getschemahivemountname, wcmconfig/ITargetInfo::GetSchemaHiveMountName
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
 - ITargetInfo::GetSchemaHiveMountName
 - wcmconfig/ITargetInfo::GetSchemaHiveMountName
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
 - ITargetInfo.GetSchemaHiveMountName
---

# ITargetInfo::GetSchemaHiveMountName


## -description

Gets the name of the mount location of the schema hive.

## -parameters

### -param pMountName [out]

The name of the mount location of the schema hive. The value of <i>pMountName</i> is <b>NULL</b>  on return if the default name is to be used.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>