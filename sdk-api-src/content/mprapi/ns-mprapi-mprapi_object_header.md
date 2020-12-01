---
UID: NS:mprapi._MPRAPI_OBJECT_HEADER
title: MPRAPI_OBJECT_HEADER (mprapi.h)
description: Defines the structure version for the RAS_CONNECTION_EX, MPR_SERVER_EX, MPR_SERVER_SET_CONFIG_EX, RAS_UPDATE_CONNECTION, AUTH_VALIDATION_EX structures, and the structure version used by the MprAdminConnectionEnumEx method.
helpviewer_keywords: ["*PMPRAPI_OBJECT_HEADER","MPRAPI_MPR_SERVER_OBJECT_REVISION_1","MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1","MPRAPI_OBJECT_HEADER","MPRAPI_OBJECT_HEADER structure [RAS]","MPRAPI_RAS_CONNECTION_OBJECT_REVISION_1","PMPRAPI_OBJECT_HEADER","PMPRAPI_OBJECT_HEADER structure pointer [RAS]","mprapi/MPRAPI_OBJECT_HEADER","mprapi/PMPRAPI_OBJECT_HEADER","rras.mprapi_object_header"]
old-location: rras\mprapi_object_header.htm
tech.root: RRAS
ms.assetid: 2f4e1ddc-7991-4091-9889-fdd2d75e702f
ms.date: 12/05/2018
ms.keywords: '*PMPRAPI_OBJECT_HEADER, MPRAPI_MPR_SERVER_OBJECT_REVISION_1, MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1, MPRAPI_OBJECT_HEADER, MPRAPI_OBJECT_HEADER structure [RAS], MPRAPI_RAS_CONNECTION_OBJECT_REVISION_1, PMPRAPI_OBJECT_HEADER, PMPRAPI_OBJECT_HEADER structure pointer [RAS], mprapi/MPRAPI_OBJECT_HEADER, mprapi/PMPRAPI_OBJECT_HEADER, rras.mprapi_object_header'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MPRAPI_OBJECT_HEADER, *PMPRAPI_OBJECT_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPRAPI_OBJECT_HEADER
 - mprapi/_MPRAPI_OBJECT_HEADER
 - PMPRAPI_OBJECT_HEADER
 - mprapi/PMPRAPI_OBJECT_HEADER
 - MPRAPI_OBJECT_HEADER
 - mprapi/MPRAPI_OBJECT_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPRAPI_OBJECT_HEADER
---

# MPRAPI_OBJECT_HEADER structure


## -description

The [RAS_UPDATE_CONNECTION](/windows/desktop/api/mprapi/ns-mprapi-ras_update_connection), <a href="/windows/desktop/api/mprapi/ns-mprapi-auth_validation_ex">AUTH_VALIDATION_EX</a> structures,  and the structure version used by the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenumex">MprAdminConnectionEnumEx</a> method.

## -struct-fields

### -field revision

A value that represents the version of the structure specified by <b>type</b>. Possible values are:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_RAS_CONNECTION_OBJECT_REVISION_1"></a><a id="mprapi_ras_connection_object_revision_1"></a><dl>
<dt><b>MPRAPI_RAS_CONNECTION_OBJECT_REVISION_1</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Represents version 1 of the <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure if <b>type</b> is <b>MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_MPR_SERVER_OBJECT_REVISION_1"></a><a id="mprapi_mpr_server_object_revision_1"></a><dl>
<dt><b>MPRAPI_MPR_SERVER_OBJECT_REVISION_1</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Represents version 1 of the <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_ex0">MPR_SERVER_EX</a> structure if <b>type</b> is <b>MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1"></a><a id="mprapi_mpr_server_set_config_object_revision_1"></a><dl>
<dt><b>MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Represents version 1 of the <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_set_config_ex0">MPR_SERVER_SET_CONFIG_EX</a> structure if <b>type</b> is <b>MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT</b>.

</td>
</tr>
</table>
 



#### type

A value from the <a href="/windows/desktop/api/mprapi/ne-mprapi-mprapi_object_type">MPRAPI_OBJECT_TYPE</a> enumeration that specifies the structure type.



#### size

The size, in bytes,  of the structure based on <b>type</b> and <b>revision</b>.

### -field type

### -field size

## -see-also

<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>