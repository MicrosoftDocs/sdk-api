---
UID: NS:mprapi._MPR_CREDENTIALSEX_0
title: MPR_CREDENTIALSEX_0 (mprapi.h)
author: windows-sdk-content
description: The MPR_CREDENTIALSEX_0 structure contains extended credentials information such as the information used by Extensible Authentication Protocols (EAPs).
old-location: rras\mpr_credentialsex_0.htm
tech.root: RRAS
ms.assetid: a1524c6e-3a94-4fc1-be28-bcaca8bcc62e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMPR_CREDENTIALSEX_0, MPR_CREDENTIALSEX_0, MPR_CREDENTIALSEX_0 structure [RAS], PMPR_CREDENTIALSEX_0, PMPR_CREDENTIALSEX_0 structure pointer [RAS], _MPR_CREDENTIALSEX_0, _mpr_mpr_credentialsex_0, mprapi/MPR_CREDENTIALSEX_0, mprapi/PMPR_CREDENTIALSEX_0, rras.mpr_credentialsex_0"
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - MPR_CREDENTIALSEX_0
product: Windows
targetos: Windows
req.typenames: MPR_CREDENTIALSEX_0, *PMPR_CREDENTIALSEX_0
req.redist: 
ms.custom: 19H1
---

# MPR_CREDENTIALSEX_0 structure


## -description


The 
<b>MPR_CREDENTIALSEX_0</b> structure contains extended credentials information such as the information used by Extensible Authentication Protocols (EAPs).


## -struct-fields




### -field dwSize

Specifies the size of the data pointed to by the <b>lpbCredentialsInfo</b> member.


### -field lpbCredentialsInfo

Pointer to the extended credentials information.


## -see-also




<a href="https://msdn.microsoft.com/0ef9f437-a15b-4f6c-ac76-4c31a23e8792">MprAdminInterfaceGetCredentialsEx</a>



<a href="https://msdn.microsoft.com/d0807c03-3994-4624-97ea-94b55e7cd1e4">MprAdminInterfaceSetCredentialsEx</a>
 

 

