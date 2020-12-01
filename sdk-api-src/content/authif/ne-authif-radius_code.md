---
UID: NE:authif._RADIUS_CODE
title: RADIUS_CODE (authif.h)
description: The RADIUS_CODE enumeration type enumerates the possible RADIUS packet codes.
helpviewer_keywords: ["RADIUS_CODE","RADIUS_CODE enumeration [Network Policy Server]","_ias_radius_code","authif/RADIUS_CODE","authif/rcAccessAccept","authif/rcAccessChallenge","authif/rcAccessReject","authif/rcAccessRequest","authif/rcAccountingRequest","authif/rcAccountingResponse","authif/rcDiscard","authif/rcUnknown","ias.radius_code","nps.IAS_radius_code","rcAccessAccept","rcAccessChallenge","rcAccessReject","rcAccessRequest","rcAccountingRequest","rcAccountingResponse","rcDiscard","rcUnknown"]
old-location: nps\IAS_radius_code.htm
tech.root: Nps
ms.assetid: cb971643-82ca-4302-a961-9d567da04c27
ms.date: 12/05/2018
ms.keywords: RADIUS_CODE, RADIUS_CODE enumeration [Network Policy Server], _ias_radius_code, authif/RADIUS_CODE, authif/rcAccessAccept, authif/rcAccessChallenge, authif/rcAccessReject, authif/rcAccessRequest, authif/rcAccountingRequest, authif/rcAccountingResponse, authif/rcDiscard, authif/rcUnknown, ias.radius_code, nps.IAS_radius_code, rcAccessAccept, rcAccessChallenge, rcAccessReject, rcAccessRequest, rcAccountingRequest, rcAccountingResponse, rcDiscard, rcUnknown
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
req.typenames: RADIUS_CODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_CODE
 - authif/_RADIUS_CODE
 - RADIUS_CODE
 - authif/RADIUS_CODE
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
 - RADIUS_CODE
---

# RADIUS_CODE enumeration


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_CODE</b> enumeration type enumerates the possible RADIUS packet codes.

## -enum-fields

### -field rcUnknown

The packet type is unrecognized. This is used to indicate that the disposition of a request is not being set by this extension DLL.

### -field rcAccessRequest

RADIUS Access-Request packet. See 
<a href="https://www.ietf.org/rfc/rfc2865.txt">RFC 2865</a> for more information.

### -field rcAccessAccept

RADIUS Access-Accept packet. See 
<a href="https://www.ietf.org/rfc/rfc2865.txt">RFC 2865</a> for more information.

### -field rcAccessReject

RADIUS Access-Reject packet. See 
<a href="https://www.ietf.org/rfc/rfc2865.txt">RFC 2865</a> for more information.

### -field rcAccountingRequest

RADIUS Accounting-Request packet. See 
<a href="https://www.ietf.org/rfc/rfc2866.txt">RFC 2866</a> for more information.

### -field rcAccountingResponse

RADIUS Accounting-Response packet. See 
<a href="https://www.ietf.org/rfc/rfc2866.txt">RFC 2866</a> for more information.

### -field rcAccessChallenge

RADIUS Access-Challenge packet. See 
<a href="https://www.ietf.org/rfc/rfc2865.txt">RFC 2865</a> for more information.

### -field rcDiscard

The packet was discarded.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-enumerations">NPS Extensions Enumerations</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/ns-authif-radius_extension_control_block">RADIUS_EXTENSION_CONTROL_BLOCK</a>



<a href="/previous-versions/ms688462(v=vs.85)">SetResponseType</a>