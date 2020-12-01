---
UID: NF:mprapi.MprConfigServerDisconnect
title: MprConfigServerDisconnect function (mprapi.h)
description: The MprConfigServerDisconnect function disconnects a connection made by a previous call to MprConfigServerConnect.
helpviewer_keywords: ["MprConfigServerDisconnect","MprConfigServerDisconnect function [RAS]","_mpr_mprconfigserverdisconnect","mprapi/MprConfigServerDisconnect","rras.mprconfigserverdisconnect"]
old-location: rras\mprconfigserverdisconnect.htm
tech.root: RRAS
ms.assetid: 71cdb26b-e9d0-414c-aff9-0eed187d08ba
ms.date: 12/05/2018
ms.keywords: MprConfigServerDisconnect, MprConfigServerDisconnect function [RAS], _mpr_mprconfigserverdisconnect, mprapi/MprConfigServerDisconnect, rras.mprconfigserverdisconnect
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprConfigServerDisconnect
 - mprapi/MprConfigServerDisconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigServerDisconnect
---

# MprConfigServerDisconnect function


## -description

The 
<b>MprConfigServerDisconnect</b> function disconnects a connection made by a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

## -parameters

### -param hMprConfig [in]

Handle to a router configuration obtained from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>