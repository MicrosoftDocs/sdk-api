---
UID: NS:lmaccess._MSA_INFO_0
title: "_MSA_INFO_0"
author: windows-sdk-content
description: Specifies information about a managed service account.
old-location: security\msa_info_0.htm
old-project: secmgmt
ms.assetid: 21e04ee8-98c9-4c78-9564-e07f5edaf847
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPMSA_INFO_0, *PMSA_INFO_0, MSA_INFO_0, MSA_INFO_0 structure [Security], PMSA_INFO_0, PMSA_INFO_0 structure pointer [Security], _MSA_INFO_0, lmaccess/MSA_INFO_0, lmaccess/PMSA_INFO_0, security.msa_info_0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSA_INFO_0, *PMSA_INFO_0, *LPMSA_INFO_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - MSA_INFO_0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MSA_INFO_0 structure


## -description


Specifies information about a managed service account. This structure is used by the <a href="https://msdn.microsoft.com/ee253cab-bd53-426e-809a-12a1ccdc010b">NetQueryServiceAccount</a> function.


## -struct-fields




### -field State

A value of the <a href="https://msdn.microsoft.com/3cba6c6a-1d63-4795-b009-1fcdf86cc2ef">MSA_INFO_STATE</a> enumeration that indicates the state of the service account specified in the call to the <a href="https://msdn.microsoft.com/ee253cab-bd53-426e-809a-12a1ccdc010b">NetQueryServiceAccount</a> function.

