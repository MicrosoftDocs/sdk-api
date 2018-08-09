---
UID: NF:wcmconfig.ITargetInfo.SetSchemaHiveMountName
title: ITargetInfo::SetSchemaHiveMountName
author: windows-sdk-content
description: Sets the name of the mount location of the schema hive.
old-location: smi\itargetinfo_setschemahivemountname.htm
old-project: smi
ms.assetid: 128cf457-c66e-49b7-88a7-3f5d87800a20
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ITargetInfo interface [SMI],SetSchemaHiveMountName method, ITargetInfo.SetSchemaHiveMountName, ITargetInfo::SetSchemaHiveMountName, SetSchemaHiveMountName, SetSchemaHiveMountName method [SMI], SetSchemaHiveMountName method [SMI],ITargetInfo interface, smi.itargetinfo_setschemahivemountname, wcmconfig/ITargetInfo::SetSchemaHiveMountName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.SetSchemaHiveMountName
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ITargetInfo::SetSchemaHiveMountName


## -description


Sets the name of the mount location of the schema hive.


## -parameters




### -param pwzMountName [in]

The mount location of the schema hive.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. May return <b>E_OUTOFMEMORY</b> if the system is low on resources.




## -see-also




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

