---
UID: NF:mi.MI_Serializer_Close
title: MI_Serializer_Close function (mi.h)
description: Closes a serializer object and frees any internal memory associated with it.
helpviewer_keywords: ["MI_Serializer_Close","MI_Serializer_Close function [Windows Management Infrastructure (MI)]","mi/MI_Serializer_Close","wmi_v2.mi_serializer_close"]
old-location: wmi_v2\mi_serializer_close.htm
tech.root: wmi_v2
ms.assetid: fbae767d-1f30-4b73-8978-ea14ce707303
ms.date: 12/05/2018
ms.keywords: MI_Serializer_Close, MI_Serializer_Close function [Windows Management Infrastructure (MI)], mi/MI_Serializer_Close, wmi_v2.mi_serializer_close
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
 - MI_Serializer_Close
 - mi/MI_Serializer_Close
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
 - MI_Serializer_Close
---

# MI_Serializer_Close function


## -description

Closes a serializer object and frees any internal memory associated with it.

## -parameters

### -param serializer [in, out]

A pointer to a serializer returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newserializer">MI_Application_NewSerializer</a> function.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

This function should be called if there are no more active calls into the serializer.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newserializer">MI_Application_NewSerializer</a>