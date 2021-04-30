---
UID: NS:ras._RAS_PROJECTION_INFO
title: RAS_PROJECTION_INFO (ras.h)
description: Contains the Point-to-Point (PPP) or Internet Key Exchange version 2 (IKEv2) projection information for a RAS connection.
helpviewer_keywords: ["*PRAS_PROJECTION_INFO","PRAS_PROJECTION_INFO","PRAS_PROJECTION_INFO structure pointer [RAS]","RAS_PROJECTION_INFO","RAS_PROJECTION_INFO structure [RAS]","ras/PRAS_PROJECTION_INFO","ras/RAS_PROJECTION_INFO","rras.ras_projection_info"]
old-location: rras\ras_projection_info.htm
tech.root: RRAS
ms.assetid: ca4fbaff-f035-4340-8d29-7dcddaf1b1bb
ms.date: 12/05/2018
ms.keywords: '*PRAS_PROJECTION_INFO, PRAS_PROJECTION_INFO, PRAS_PROJECTION_INFO structure pointer [RAS], RAS_PROJECTION_INFO, RAS_PROJECTION_INFO structure [RAS], ras/PRAS_PROJECTION_INFO, ras/RAS_PROJECTION_INFO, rras.ras_projection_info'
req.header: ras.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RAS_PROJECTION_INFO, *PRAS_PROJECTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_PROJECTION_INFO
 - ras/_RAS_PROJECTION_INFO
 - PRAS_PROJECTION_INFO
 - ras/PRAS_PROJECTION_INFO
 - RAS_PROJECTION_INFO
 - ras/RAS_PROJECTION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ras.h
api_name:
 - RAS_PROJECTION_INFO
---

# RAS_PROJECTION_INFO structure


## -description

The <b>RAS_PROJECTION_INFO</b> structure contains the  Point-to-Point (PPP) or Internet Key Exchange version 2 (IKEv2) projection information for a RAS connection.

## -struct-fields

### -field version

A <a href="/previous-versions/windows/desktop/legacy/dd408102(v=vs.85)">RASAPIVERSION</a> value that specifies the structure version.

### -field type

A <a href="/windows/desktop/api/ras/ne-ras-rasprojection_info_type">RASPROJECTION_INFO_TYPE</a> value that specifies the connection type in <b>union</b>.

### -field ppp

### -field ikev2

 




#### - union



#### ppp

A <a href="/windows/desktop/api/ras/ns-ras-rasppp_projection_info">RASPPP_PROJECTION_INFO</a> structure that contains the PPP projection information of a RAS connection.



#### ikev2

A <a href="/windows/desktop/api/ras/ns-ras-rasikev2_projection_info">RASIKEV2_PROJECTION_INFO</a> structure that contains the IKEv2 projection information of a RAS connection.

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rasgetprojectioninfoex">RasGetProjectionInfoEx</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-structures">Remote Access Service Structures</a>