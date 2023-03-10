---
UID: NS:ras.tagRASDEVSPECIFICINFO
title: RASDEVSPECIFICINFO (ras.h)
description: Used to send a cookie for server validation and bypass point-to-point (PPP) authentication.
helpviewer_keywords: ["*PRASDEVSPECIFICINFO","PRASDEVSPECIFICINFO","PRASDEVSPECIFICINFO structure pointer [RAS]","RASDEVSPECIFICINFO","RASDEVSPECIFICINFO structure [RAS]","ras/PRASDEVSPECIFICINFO","ras/RASDEVSPECIFICINFO","rras.rasdevspecificinfo"]
old-location: rras\rasdevspecificinfo.htm
tech.root: RRAS
ms.assetid: 0dee3f10-d49b-4059-8cfb-c28af6b8b371
ms.date: 12/05/2018
ms.keywords: '*PRASDEVSPECIFICINFO, PRASDEVSPECIFICINFO, PRASDEVSPECIFICINFO structure pointer [RAS], RASDEVSPECIFICINFO, RASDEVSPECIFICINFO structure [RAS], ras/PRASDEVSPECIFICINFO, ras/RASDEVSPECIFICINFO, rras.rasdevspecificinfo'
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
req.typenames: RASDEVSPECIFICINFO, *PRASDEVSPECIFICINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRASDEVSPECIFICINFO
 - ras/tagRASDEVSPECIFICINFO
 - PRASDEVSPECIFICINFO
 - ras/PRASDEVSPECIFICINFO
 - RASDEVSPECIFICINFO
 - ras/RASDEVSPECIFICINFO
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
 - RASDEVSPECIFICINFO
---

# RASDEVSPECIFICINFO structure


## -description

The <b>RASDEVSPECIFICINFO</b> structure is used to send a cookie for server validation and bypass point-to-point (PPP) authentication.

## -struct-fields

### -field dwSize

The size, in bytes, of the cookie in <b>pbDevSpecificInfo</b>.

### -field pbDevSpecificInfo

A pointer to a BLOB that contains the authentication cookie.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-structures">Remote Access Service Structures</a>