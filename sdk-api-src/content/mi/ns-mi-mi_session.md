---
UID: NS:mi._MI_Session
title: MI_Session (mi.h)
description: An object that is associated with a destination and has a set of credentials and options associated with it. .
helpviewer_keywords: ["MI_Session","MI_Session structure [Windows Management Infrastructure (MI)]","mi/MI_Session","wmi._mi_session","wmi_v2.mi_session"]
old-location: wmi_v2\mi_session.htm
tech.root: wmi_v2
ms.assetid: 68a69321-0aa9-423e-a72f-aa2f4dee2d51
ms.date: 12/05/2018
ms.keywords: MI_Session, MI_Session structure [Windows Management Infrastructure (MI)], mi/MI_Session, wmi._mi_session, wmi_v2.mi_session
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
req.typenames: MI_Session
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Session
 - mi/_MI_Session
 - MI_Session
 - mi/MI_Session
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
 - MI_Session
---

# MI_Session structure


## -description

An object that is associated with a destination and has a set of credentials and options associated with it. .

## -struct-fields

### -field reserved1

For internal use only.

### -field reserved2

For internal use only.

### -field ft

This is the function table for accessing carrying out 
                      operations on a destination machine, along with configuration of the session. Use the functions containing the MI_Session_ prefix to access this information.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocalsession">MI_Context_GetLocalSession</a>