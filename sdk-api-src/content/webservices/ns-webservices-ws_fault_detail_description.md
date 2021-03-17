---
UID: NS:webservices._WS_FAULT_DETAIL_DESCRIPTION
title: WS_FAULT_DETAIL_DESCRIPTION (webservices.h)
description: A description of the detail element of a fault message.
helpviewer_keywords: ["WS_FAULT_DETAIL_DESCRIPTION","WS_FAULT_DETAIL_DESCRIPTION structure [Web Services for Windows]","webservices/WS_FAULT_DETAIL_DESCRIPTION","wsw.ws_fault_detail_description"]
old-location: wsw\ws_fault_detail_description.htm
tech.root: wsw
ms.assetid: 5a89ca26-63c7-414a-a27d-019c5b020f63
ms.date: 12/05/2018
ms.keywords: WS_FAULT_DETAIL_DESCRIPTION, WS_FAULT_DETAIL_DESCRIPTION structure [Web Services for Windows], webservices/WS_FAULT_DETAIL_DESCRIPTION, wsw.ws_fault_detail_description
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_FAULT_DETAIL_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_FAULT_DETAIL_DESCRIPTION
 - webservices/_WS_FAULT_DETAIL_DESCRIPTION
 - WS_FAULT_DETAIL_DESCRIPTION
 - webservices/WS_FAULT_DETAIL_DESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_FAULT_DETAIL_DESCRIPTION
---

# WS_FAULT_DETAIL_DESCRIPTION structure


## -description

A description of the detail element of a fault message.

## -struct-fields

### -field action

The action associated with the fault message.
                

If the message does not have an action, this field can be <b>NULL</b>.

### -field detailElementDescription

The description of the fault detail of the fault.  This 
                    field must be specified (it may not be <b>NULL</b>).

## -remarks

The fault description defines the action of the fault message
                along with a description of the detail element that is
                contained within the fault.
            

The fault description can be used to set and get the
                fault detail element stored within a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object
                using <a href="/windows/desktop/api/webservices/nf-webservices-wssetfaulterrordetail">WsSetFaultErrorDetail</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsgetfaulterrordetail">WsGetFaultErrorDetail</a>.