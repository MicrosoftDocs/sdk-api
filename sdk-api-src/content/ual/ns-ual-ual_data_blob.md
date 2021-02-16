---
UID: NS:ual.tagUAL_DATA_BLOB
title: UAL_DATA_BLOB (ual.h)
description: Specifies information about a User Access Logging (UAL) session.
helpviewer_keywords: ["*PUAL_DATA_BLOB","PUAL_DATA_BLOB","PUAL_DATA_BLOB structure pointer [User Access Logging]","UAL_DATA_BLOB","UAL_DATA_BLOB structure [User Access Logging]","ual.ual_data_blob","ual/PUAL_DATA_BLOB","ual/UAL_DATA_BLOB"]
old-location: ual\ual_data_blob.htm
tech.root: ual
ms.assetid: 5C191327-0D15-41D7-8218-73F387740FDF
ms.date: 12/05/2018
ms.keywords: '*PUAL_DATA_BLOB, PUAL_DATA_BLOB, PUAL_DATA_BLOB structure pointer [User Access Logging], UAL_DATA_BLOB, UAL_DATA_BLOB structure [User Access Logging], ual.ual_data_blob, ual/PUAL_DATA_BLOB, ual/UAL_DATA_BLOB'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UAL_DATA_BLOB, *PUAL_DATA_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUAL_DATA_BLOB
 - ual/tagUAL_DATA_BLOB
 - PUAL_DATA_BLOB
 - ual/PUAL_DATA_BLOB
 - UAL_DATA_BLOB
 - ual/UAL_DATA_BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ual.h
api_name:
 - UAL_DATA_BLOB
---

# UAL_DATA_BLOB structure


## -description

Specifies information about a User Access Logging (UAL) session.

## -struct-fields

### -field Size

The size, in bytes, of this structure.

### -field RoleGuid

A <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that represents the role or minor product name associated with a UAL session.

### -field TenantId

A <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies a tenant of a hosted environment. This can be used to differentiate client tenants when more than one tenant uses the same host service.

### -field Address

The IP address of the client that accompanies the UAL payload from installed roles and products.

### -field UserName

The name of the client user that accompanies the UAL payload from installed roles and products..

## -see-also

<a href="/previous-versions/windows/desktop/api/ual/nf-ual-ualinstrument">UalInstrument</a>



<a href="/previous-versions/windows/desktop/api/ual/nf-ual-ualstart">UalStart</a>



<a href="/previous-versions/windows/desktop/api/ual/nf-ual-ualstop">UalStop</a>