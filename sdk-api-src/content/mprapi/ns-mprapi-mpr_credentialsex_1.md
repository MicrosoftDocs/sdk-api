---
UID: NS:mprapi._MPR_CREDENTIALSEX_1
title: MPR_CREDENTIALSEX_1
author: windows-sdk-content
description: The MPR_CREDENTIALSEX_1 structure contains a pre-shared key used by a demand-dial interface.
old-location: rras\mpr_credentialsex_1.htm
tech.root: rras
ms.assetid: b37b9589-5c25-44ac-954a-c9fb2c2ee503
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMPR_CREDENTIALSEX_1, MPR_CREDENTIALSEX_1, MPR_CREDENTIALSEX_1 structure [RAS], PMPR_CREDENTIALSEX_1, PMPR_CREDENTIALSEX_1 structure pointer [RAS], _MPR_CREDENTIALSEX_1, _mpr_mpr_credentialsex_1, mprapi/MPR_CREDENTIALSEX_1, mprapi/PMPR_CREDENTIALSEX_1, rras.mpr_credentialsex_1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_CREDENTIALSEX_1
product: Windows
targetos: Windows
req.typenames: MPR_CREDENTIALSEX_1, *PMPR_CREDENTIALSEX_1
req.redist: 
---

# MPR_CREDENTIALSEX_1 structure


## -description


The 
<b>MPR_CREDENTIALSEX_1</b> structure contains a pre-shared key used by a demand-dial interface.


## -struct-fields




### -field dwSize

Specifies the size of the data pointed to by the <b>lpbCredentialsInfo</b> member.


### -field lpbCredentialsInfo

Pointer to the pre-shared key.


## -remarks



To a delete a pre-shared key, call 
<a href="https://msdn.microsoft.com/a5372bfb-185c-4562-afa3-35399c8e2a46">MprAdminInterfaceSetCredentials</a> with the <b>MPR_CREDENTIALSEX_1.dwSize</b> member set to zero.




## -see-also




<a href="https://msdn.microsoft.com/0ef9f437-a15b-4f6c-ac76-4c31a23e8792">MprAdminInterfaceGetCredentialsEx</a>



<a href="https://msdn.microsoft.com/d0807c03-3994-4624-97ea-94b55e7cd1e4">MprAdminInterfaceSetCredentialsEx</a>
 

 

