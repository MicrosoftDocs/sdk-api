---
UID: NC:authif.PRADIUS_EXTENSION_INIT
title: PRADIUS_EXTENSION_INIT (authif.h)
description: The RadiusExtensionInit function is an application-defined function and is called by NPS while the service is starting up. Use RadiusExtensionInit to perform any initialization operations for the Extension DLL.
helpviewer_keywords: ["PRADIUS_EXTENSION_INIT","PRADIUS_EXTENSION_INIT callback","PRADIUS_EXTENSION_INIT callback function [Network Policy Server]","RadiusExtensionInit","_ias_radiusextensioninit","authif/PRADIUS_EXTENSION_INIT","ias.radiusextensioninit","nps.IAS_radiusextensioninit"]
old-location: nps\IAS_radiusextensioninit.htm
tech.root: Nps
ms.assetid: a463927f-550d-4078-8c0f-35c8742d887a
ms.date: 12/05/2018
ms.keywords: PRADIUS_EXTENSION_INIT, PRADIUS_EXTENSION_INIT callback, PRADIUS_EXTENSION_INIT callback function [Network Policy Server], RadiusExtensionInit, _ias_radiusextensioninit, authif/PRADIUS_EXTENSION_INIT, ias.radiusextensioninit, nps.IAS_radiusextensioninit
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PRADIUS_EXTENSION_INIT
 - authif/PRADIUS_EXTENSION_INIT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - AuthIf.h
api_name:
 - PRADIUS_EXTENSION_INIT
---

# PRADIUS_EXTENSION_INIT callback function


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RadiusExtensionInit</b> function is an application-defined function and is called by NPS while the service is starting up. Use 
<b>RadiusExtensionInit</b> to perform any initialization operations for the Extension DLL.

## -parameters

### -param unnamedParam1

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from WinError.h.

## -remarks

A return value other then <b>NO_ERROR</b> will cause NPS to fail to start.

<b>RadiusExtensionInit</b> is an optional function. The RADIUS Extension DLL need not implement 
<b>RadiusExtensionInit</b>.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-functions">NPS Extensions Functions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_term">RadiusExtensionTerm</a>