---
UID: NF:wcmconfig.ITargetInfo.GetSchemaHiveMountName
title: ITargetInfo::GetSchemaHiveMountName
author: windows-sdk-content
description: Gets the name of the mount location of the schema hive.
old-location: smi\itargetinfo_getschemahivemountname.htm
old-project: SMI
ms.assetid: d63e3f49-bb7b-4ef6-a573-811b9bbdd9b0
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetSchemaHiveMountName, GetSchemaHiveMountName method [SMI], GetSchemaHiveMountName method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],GetSchemaHiveMountName method, ITargetInfo.GetSchemaHiveMountName, ITargetInfo::GetSchemaHiveMountName, smi.itargetinfo_getschemahivemountname, wcmconfig/ITargetInfo::GetSchemaHiveMountName
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
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	ITargetInfo.GetSchemaHiveMountName
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

