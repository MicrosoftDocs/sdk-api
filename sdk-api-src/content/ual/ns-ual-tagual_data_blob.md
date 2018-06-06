---
UID: NS:ual.tagUAL_DATA_BLOB
title: tagUAL_DATA_BLOB
author: windows-sdk-content
description: Specifies information about a User Access Logging (UAL) session.
old-location: ual\ual_data_blob.htm
old-project: ual
ms.assetid: 5C191327-0D15-41D7-8218-73F387740FDF
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PUAL_DATA_BLOB, PUAL_DATA_BLOB, PUAL_DATA_BLOB structure pointer [User Access Logging], UAL_DATA_BLOB, UAL_DATA_BLOB structure [User Access Logging], tagUAL_DATA_BLOB, ual.ual_data_blob, ual/PUAL_DATA_BLOB, ual/UAL_DATA_BLOB"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ual.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: UAL_DATA_BLOB, *PUAL_DATA_BLOB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ual.h
api_name:
 - UAL_DATA_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# tagUAL_DATA_BLOB structure


## -description


Specifies information about a User Access Logging (UAL) session.


## -struct-fields




### -field Size

The size, in bytes, of this structure.


### -field RoleGuid

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that represents the role or minor product name associated with a UAL session.


### -field TenantId

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that identifies a tenant of a hosted environment. This can be used to differentiate client tenants when more than one tenant uses the same host service.


### -field Address

The IP address of the client that accompanies the UAL payload from installed roles and products.


### -field UserName

The name of the client user that accompanies the UAL payload from installed roles and products..


## -see-also




<a href="https://msdn.microsoft.com/C7A0340F-3250-4570-9672-FC78AFC9ECC6">UalInstrument</a>



<a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a>



<a href="https://msdn.microsoft.com/142A0C96-2D53-4C31-9847-D6D5313C841E">UalStop</a>
 

 

