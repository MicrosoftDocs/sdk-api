---
UID: NC:authif.PRADIUS_EXTENSION_TERM
title: PRADIUS_EXTENSION_TERM (authif.h)
description: The RadiusExtensionTerm function is an application-defined function and is called by NPS prior to unloading the Extension DLL. Use RadiusExtensionTerm to perform any clean-up operations for the Extension DLL.
helpviewer_keywords: ["PRADIUS_EXTENSION_TERM","PRADIUS_EXTENSION_TERM callback","PRADIUS_EXTENSION_TERM callback function [Network Policy Server]","RadiusExtensionTerm","_ias_radiusextensionterm","authif/PRADIUS_EXTENSION_TERM","ias.radiusextensionterm","nps.IAS_radiusextensionterm"]
old-location: nps\IAS_radiusextensionterm.htm
tech.root: Nps
ms.assetid: a3f6669f-bad5-4289-abbc-633851c1f5f8
ms.date: 03/20/2023
ms.keywords: PRADIUS_EXTENSION_TERM, PRADIUS_EXTENSION_TERM callback, PRADIUS_EXTENSION_TERM callback function [Network Policy Server], RadiusExtensionTerm, _ias_radiusextensionterm, authif/PRADIUS_EXTENSION_TERM, ias.radiusextensionterm, nps.IAS_radiusextensionterm
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
 - PRADIUS_EXTENSION_TERM
 - authif/PRADIUS_EXTENSION_TERM
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
 - PRADIUS_EXTENSION_TERM
---

# PRADIUS_EXTENSION_TERM callback function

## -description

> [!NOTE]
> Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008. The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.

The **RadiusExtensionTerm** function is an application-defined function and is called by NPS prior to unloading the Extension DLL. Use **RadiusExtensionTerm** to perform any clean-up operations for the Extension DLL.

## -remarks

**RadiusExtensionTerm** is an optional function. The RADIUS Extension DLL need not implement **RadiusExtensionTerm**.

## -see-also

[About NPS Extensions](/windows/win32/Nps/ias-about-internet-authentication-service)

[NPS Extensions Functions](/windows/win32/Nps/ias-internet-authentication-service-functions)

[NPS Extensions Reference](/windows/win32/Nps/ias-internet-authentication-service-reference)

[RadiusExtensionInit](/windows/win32/api/authif/nc-authif-pradius_extension_init)
