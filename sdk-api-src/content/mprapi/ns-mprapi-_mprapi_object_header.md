---
UID: NS:mprapi._MPRAPI_OBJECT_HEADER
title: "_MPRAPI_OBJECT_HEADER"
author: windows-sdk-content
description: Defines the structure version for the RAS_CONNECTION_EX, MPR_SERVER_EX, MPR_SERVER_SET_CONFIG_EX, RAS_UPDATE_CONNECTION, AUTH_VALIDATION_EX structures, and the structure version used by the MprAdminConnectionEnumEx method.
old-location: rras\mprapi_object_header.htm
tech.root: RRAS
ms.assetid: 2f4e1ddc-7991-4091-9889-fdd2d75e702f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PMPRAPI_OBJECT_HEADER, MPRAPI_MPR_SERVER_OBJECT_REVISION_1, MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1, MPRAPI_OBJECT_HEADER, MPRAPI_OBJECT_HEADER structure [RAS], MPRAPI_RAS_CONNECTION_OBJECT_REVISION_1, PMPRAPI_OBJECT_HEADER, PMPRAPI_OBJECT_HEADER structure pointer [RAS], _MPRAPI_OBJECT_HEADER, mprapi/MPRAPI_OBJECT_HEADER, mprapi/PMPRAPI_OBJECT_HEADER, rras.mprapi_object_header"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPRAPI_OBJECT_HEADER
product: Windows
targetos: Windows
req.typenames: MPRAPI_OBJECT_HEADER, *PMPRAPI_OBJECT_HEADER
req.redist: 
---

# _MPRAPI_OBJECT_HEADER structure


## -description


The <b>MPRAPI_OBJECT_HEADER</b> structure is used as a header field for structures and defines the structure version for the <a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a>, <a href="https://msdn.microsoft.com/10c1e3bd-adb8-4aff-835c-e7d881c9f5cf">MPR_SERVER_EX</a>, <a href="https://msdn.microsoft.com/6c993c9c-4522-4758-926a-fa7ef2a89418">MPR_SERVER_SET_CONFIG_EX</a>, <a href="https://msdn.microsoft.com/bfa35f1c-e9f5-43f1-ad2d-d54f4675cff8">RAS_UPDATE_CONNECTION</a>, <a href="https://msdn.microsoft.com/17e78379-a9f8-4aab-aff3-aa9b21eb629c">AUTH_VALIDATION_EX</a> structures,  and the structure version used by the <a href="https://msdn.microsoft.com/12507432-bf18-444d-9bcc-4ebc1418c083">MprAdminConnectionEnumEx</a> method.


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
Represents version 1 of the <a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure if <b>type</b> is <b>MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_MPR_SERVER_OBJECT_REVISION_1"></a><a id="mprapi_mpr_server_object_revision_1"></a><dl>
<dt><b>MPRAPI_MPR_SERVER_OBJECT_REVISION_1</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Represents version 1 of the <a href="https://msdn.microsoft.com/10c1e3bd-adb8-4aff-835c-e7d881c9f5cf">MPR_SERVER_EX</a> structure if <b>type</b> is <b>MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1"></a><a id="mprapi_mpr_server_set_config_object_revision_1"></a><dl>
<dt><b>MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Represents version 1 of the <a href="https://msdn.microsoft.com/6c993c9c-4522-4758-926a-fa7ef2a89418">MPR_SERVER_SET_CONFIG_EX</a> structure if <b>type</b> is <b>MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT</b>.

</td>
</tr>
</table>
 



#### type

A value from the <a href="https://msdn.microsoft.com/93d5bf41-e0ec-4dcf-b784-bbd9746f8134">MPRAPI_OBJECT_TYPE</a> enumeration that specifies the structure type.



#### size

The size, in bytes,  of the structure based on <b>type</b> and <b>revision</b>.


### -field type

 


### -field size

 




## -see-also




<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

