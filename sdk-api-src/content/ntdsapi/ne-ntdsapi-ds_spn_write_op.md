---
UID: NE:ntdsapi.DS_SPN_WRITE_OP
title: DS_SPN_WRITE_OP
author: windows-sdk-content
description: The DS_SPN_WRITE_OP enumeration identifies the type of write operation that should be performed by the DsWriteAccountSpn function.
old-location: ad\ds_spn_write_op.htm
old-project: ad
ms.assetid: 8367bdaf-3d8d-46b3-9d03-b9753e8e5a1a
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DS_SPN_ADD_SPN_OP, DS_SPN_DELETE_SPN_OP, DS_SPN_REPLACE_SPN_OP, DS_SPN_WRITE_OP, DS_SPN_WRITE_OP enumeration [Active Directory], _glines_ds_spn_write_op, ad.ds__spn__write__op, ad.ds_spn_write_op, ntdsapi/DS_SPN_ADD_SPN_OP, ntdsapi/DS_SPN_DELETE_SPN_OP, ntdsapi/DS_SPN_REPLACE_SPN_OP, ntdsapi/DS_SPN_WRITE_OP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DS_SPN_WRITE_OP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_SPN_WRITE_OP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: Any level
req.product: Rights Management Services client 1.0 or later
---

# DS_SPN_WRITE_OP enumeration


## -description


The <b>DS_SPN_WRITE_OP</b> enumeration identifies the type of write operation that should be performed by the <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a> function.


## -enum-fields




### -field DS_SPN_ADD_SPN_OP

Adds the specified service principal names (SPNs) to the object identified by the <i>pszAccount</i> parameter in <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a>.


### -field DS_SPN_REPLACE_SPN_OP

Removes all SPNs currently registered on the account identified by the <i>pszAccount</i> parameter in <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a> and replaces them with the SPNs specified  by the <i>rpszSpn</i> parameter in <b>DsWriteAccountSpn</b>.


### -field DS_SPN_DELETE_SPN_OP

Deletes the specified SPNs from the object identified by the <i>pszAccount</i> parameter in <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a>.


## -see-also




<a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

