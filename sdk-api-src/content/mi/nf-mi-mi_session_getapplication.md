---
UID: NF:mi.MI_Session_GetApplication
title: MI_Session_GetApplication function (mi.h)
description: Gets the application handle that was used to create the specified session.
helpviewer_keywords: ["MI_Session_GetApplication","MI_Session_GetApplication function [Windows Management Infrastructure (MI)]","mi/MI_Session_GetApplication","wmi_v2.mi_session_getapplication"]
old-location: wmi_v2\mi_session_getapplication.htm
tech.root: wmi_v2
ms.assetid: f368a88e-c610-42f4-8324-1bc297edf564
ms.date: 12/05/2018
ms.keywords: MI_Session_GetApplication, MI_Session_GetApplication function [Windows Management Infrastructure (MI)], mi/MI_Session_GetApplication, wmi_v2.mi_session_getapplication
req.header: mi.h
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Session_GetApplication
 - mi/MI_Session_GetApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Session_GetApplication
---

# MI_Session_GetApplication function


## -description

Gets the application handle that was used to create the specified session.

## -parameters

### -param session [in]

Session that was created from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>.

### -param application [out]

Returned copy of the application handle that was used to create the specified session.