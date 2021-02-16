---
UID: NE:mi._MI_CallbackMode
title: MI_CallbackMode (mi.h)
description: Defines the callback mode for the CIM extensions for WriteError and PromptUser functions.
helpviewer_keywords: ["MI_CALLBACKMODE_INQUIRE","MI_CALLBACKMODE_REPORT","MI_CallbackMode","MI_CallbackMode enumeration [Windows Management Infrastructure (MI)]","mi/MI_CALLBACKMODE_INQUIRE","mi/MI_CALLBACKMODE_REPORT","mi/MI_CallbackMode","wmi._mi_callbackmode","wmi_v2.mi_callbackmode"]
old-location: wmi_v2\mi_callbackmode.htm
tech.root: wmi_v2
ms.assetid: 742610a4-3276-4bab-877d-8e74c6dc80cd
ms.date: 12/05/2018
ms.keywords: MI_CALLBACKMODE_INQUIRE, MI_CALLBACKMODE_REPORT, MI_CallbackMode, MI_CallbackMode enumeration [Windows Management Infrastructure (MI)], mi/MI_CALLBACKMODE_INQUIRE, mi/MI_CALLBACKMODE_REPORT, mi/MI_CallbackMode, wmi._mi_callbackmode, wmi_v2.mi_callbackmode
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
req.typenames: MI_CallbackMode
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_CallbackMode
 - mi/_MI_CallbackMode
 - MI_CallbackMode
 - mi/MI_CallbackMode
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
 - MI_CallbackMode
---

# MI_CallbackMode enumeration


## -description

Defines the callback mode  for the CIM extensions for <b>WriteError</b> and <b>PromptUser</b> functions.

## -enum-fields

### -field MI_CALLBACKMODE_REPORT

Report the details to the client, but the provider will receive a preconfigured response.  The provider does not wait for the client to receive the request before continuing.

### -field MI_CALLBACKMODE_INQUIRE

Query the  client to determine whether  the provider should continue.

### -field MI_CALLBACKMODE_IGNORE

