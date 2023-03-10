---
UID: NF:mi.MI_Application_NewDestinationOptions
title: MI_Application_NewDestinationOptions function (mi.h)
description: Creates an MI_DestinationOptions object that can be used with the MI_Application_NewSession function.
helpviewer_keywords: ["MI_Application_NewDestinationOptions","MI_Application_NewDestinationOptions function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewDestinationOptions","wmi_v2.mi_application_newdestinationoptions"]
old-location: wmi_v2\mi_application_newdestinationoptions.htm
tech.root: wmi_v2
ms.assetid: efaa1244-7fe4-4484-b9ac-e7309e2012b6
ms.date: 12/05/2018
ms.keywords: MI_Application_NewDestinationOptions, MI_Application_NewDestinationOptions function [Windows Management Infrastructure (MI)], mi/MI_Application_NewDestinationOptions, wmi_v2.mi_application_newdestinationoptions
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
 - MI_Application_NewDestinationOptions
 - mi/MI_Application_NewDestinationOptions
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
 - MI_Application_NewDestinationOptions
---

# MI_Application_NewDestinationOptions function


## -description

Creates an <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object that can be used with the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>  function.

## -parameters

### -param application [in]

Handle returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a>.

### -param options [out]

Options container that is returned from this function.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

Destination options are used to store the configuration associated with connecting to the destination computer.  The available options can vary depending on the underlying protocol.  If the session and operations on that session just need to work with the current thread identity (or process if thread is not impersonating), then additional settings may not be needed.

Options must be closed by a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_delete">MI_DestinationOptions_Delete</a>.