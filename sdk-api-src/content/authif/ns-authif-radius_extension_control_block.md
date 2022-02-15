---
UID: NS:authif._RADIUS_EXTENSION_CONTROL_BLOCK
title: RADIUS_EXTENSION_CONTROL_BLOCK (authif.h)
description: The RADIUS_EXTENSION_CONTROL_BLOCK structure provides information about the current RADIUS request. It also provides functions for obtaining the attributes associated with the request, and for setting the disposition of the request.
helpviewer_keywords: ["*PRADIUS_EXTENSION_CONTROL_BLOCK","PRADIUS_EXTENSION_CONTROL_BLOCK","PRADIUS_EXTENSION_CONTROL_BLOCK structure pointer [Network Policy Server]","RADIUS_EXTENSION_CONTROL_BLOCK","RADIUS_EXTENSION_CONTROL_BLOCK structure [Network Policy Server]","_ias_radius_extension_control_block","authif/PRADIUS_EXTENSION_CONTROL_BLOCK","authif/RADIUS_EXTENSION_CONTROL_BLOCK","ias.radius_extension_control_block","nps.IAS_radius_extension_control_block"]
old-location: nps\IAS_radius_extension_control_block.htm
tech.root: Nps
ms.assetid: 13ff0645-d3f8-4220-a5bc-11bb515bca95
ms.date: 12/05/2018
ms.keywords: '*PRADIUS_EXTENSION_CONTROL_BLOCK, PRADIUS_EXTENSION_CONTROL_BLOCK, PRADIUS_EXTENSION_CONTROL_BLOCK structure pointer [Network Policy Server], RADIUS_EXTENSION_CONTROL_BLOCK, RADIUS_EXTENSION_CONTROL_BLOCK structure [Network Policy Server], _ias_radius_extension_control_block, authif/PRADIUS_EXTENSION_CONTROL_BLOCK, authif/RADIUS_EXTENSION_CONTROL_BLOCK, ias.radius_extension_control_block, nps.IAS_radius_extension_control_block'
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RADIUS_EXTENSION_CONTROL_BLOCK, *PRADIUS_EXTENSION_CONTROL_BLOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_EXTENSION_CONTROL_BLOCK
 - authif/_RADIUS_EXTENSION_CONTROL_BLOCK
 - PRADIUS_EXTENSION_CONTROL_BLOCK
 - authif/PRADIUS_EXTENSION_CONTROL_BLOCK
 - RADIUS_EXTENSION_CONTROL_BLOCK
 - authif/RADIUS_EXTENSION_CONTROL_BLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_EXTENSION_CONTROL_BLOCK
---

# RADIUS_EXTENSION_CONTROL_BLOCK structure


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_EXTENSION_CONTROL_BLOCK</b> structure provides information about the current RADIUS request. It also provides functions for obtaining the attributes associated with the request, and for setting the disposition of the request.

## -struct-fields

### -field cbSize

Specifies the size of the structure.

### -field dwVersion

Specifies the version of the structure.

### -field repPoint

Specifies a value of type 
<a href="/windows/desktop/api/authif/ne-authif-radius_extension_point">RADIUS_EXTENSION_POINT</a> that indicates at what point in the request process 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> was called.

### -field rcRequestType

Specifies a value of type 
<a href="/windows/desktop/api/authif/ne-authif-radius_code">RADIUS_CODE</a> that specifies the type of RADIUS request received by the Internet Authentication Service server.

### -field rcResponseType

Specifies a value of type 
<a href="/windows/desktop/api/authif/ne-authif-radius_code">RADIUS_CODE</a> that indicates the disposition of the RADIUS request.

### -field GetRequest

Pointer to the <a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> function provided by NPS. NPS sets the value of this member.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> function returns the attributes received in the RADIUS request process and any internal attributes describing the request state.

The Extension DLL can modify the attributes in the RADIUS request. For example, if NPS is acting as a RADIUS proxy, an Extension DLL could filter which attributes are forwarded to the remote RADIUS server.

To modify the attributes, the Extension DLL uses the functions provided as members of the 
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute_array">RADIUS_ATTRIBUTE_ARRAY</a> structure.



#### This

Pointer to a 
<b>RADIUS_EXTENSION_CONTROL_BLOCK</b> structure. NPS passes the Extension DLL a pointer to this structure when it calls the 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> structure.

### -field GetResponse

Pointer to the <a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> function provided by NPS. NPS sets the value of this member.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> function returns the attributes received in the RADIUS request process and any internal attributes describing the request state.

An Extension DLL can use 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> to retrieve and modify the attributes for any valid response type regardless of the request's current disposition. For example, an Extension DLL could 
<a href="/previous-versions/ms688462(v=vs.85)">set the response type</a> to rcAccessAccept, but still add attributes to those returned in the case of an rcAccessReject. The response specified by the Extension DLL (rcAccessAccept in this example) could be overridden during further processing.

To modify the attributes, the Extension DLL uses the functions provided as members of the 
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute_array">RADIUS_ATTRIBUTE_ARRAY</a> structure.



#### This

Pointer to a 
<b>RADIUS_EXTENSION_CONTROL_BLOCK</b> structure. NPS passes the Extension DLL a pointer to this structure when it calls the 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> function.



#### rcResponseType

Specifies the response type. This parameter must be one of the values enumerated by the 
<a href="/windows/desktop/api/authif/ne-authif-radius_code">RADIUS_CODE</a> enumeration type. Otherwise, the function fails, returning <b>NULL</b>.

### -field SetResponseType

Pointer to the <a href="/previous-versions/ms688462(v=vs.85)">SetResponseType</a> function provided by NPS. NPS sets the value of this member.

The 
<a href="/previous-versions/ms688462(v=vs.85)">SetResponseType</a> function sets the final disposition of the request.

Note that the disposition set by the Extension DLL can be overridden during further processing. For example, the Extension DLL may set the response type to <b>rcAccessAccept</b>, but during further processing, the response can be changed to <b>rcAccessReject</b>.



#### This

Pointer to a 
<b>RADIUS_EXTENSION_CONTROL_BLOCK</b> structure. NPS passes the Extension DLL a pointer to this structure when it calls the 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> function.



#### rcResponseType

Specifies the response type. This parameter must be one of the values contained within the 
<a href="/windows/desktop/api/authif/ne-authif-radius_code">RADIUS_CODE</a> enumerated type and is related to the <b>rcRequestType</b> member of the <b>RADIUS_EXTENSION_CONTROL_BLOCK</b> structure. If <b>rcRequestType</b> equals <b>rcAccessRequest</b>,  this value may be <b>rcAccessAccept</b>, <b>rcAccessReject</b>, <b>rcAccessChallenge</b>, or <b>rcDiscard</b>. If <b>rcRequestType</b> equals <b>rcAccountingRequest</b>, this value can be <b>rcAccountingResponse</b> or <b>rcDiscard</b>. Otherwise, the function fails, returning <b>ERROR_INVALID_PARAMETER</b>.

## -remarks

The Extension DLL must not modify this structure. Changes to the array of attributes should be made by calling the functions provided as members of this structure.

NPS passes this structure to the Extension DLL when it calls the Extension DLL's implementation of 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a>.

## -see-also

<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a>



<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a>



<a href="/windows/desktop/api/authif/ns-authif-radius_attribute_array">RADIUS_ATTRIBUTE_ARRAY</a>



<a href="/previous-versions/ms688462(v=vs.85)">SetResponseType</a>