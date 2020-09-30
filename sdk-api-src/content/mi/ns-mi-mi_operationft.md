---
UID: NS:mi._MI_OperationFT
title: MI_OperationFT (mi.h)
description: A support structure used in the MI_Operation structure. Use the functions with the name prefix &quot;MI_Operation_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_OperationFT","MI_OperationFT structure [Windows Management Infrastructure (MI)]","mi/MI_OperationFT","wmi_v2.mi_operationft"]
old-location: wmi_v2\mi_operationft.htm
tech.root: wmi_v2
ms.assetid: 925cd972-61fc-466d-a2a6-e315ef3fc499
ms.date: 12/05/2018
ms.keywords: MI_OperationFT, MI_OperationFT structure [Windows Management Infrastructure (MI)], mi/MI_OperationFT, wmi_v2.mi_operationft
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
req.typenames: MI_OperationFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_OperationFT
 - mi/_MI_OperationFT
 - MI_OperationFT
 - mi/MI_OperationFT
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
 - MI_OperationFT
---

## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_operation">MI_Operation</a> 
     structure.  Use the functions with the name prefix "MI_Operation_" to manipulate these 
     structures.

## -struct-fields

### -field Cancel

Cancels a running operation. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>.

### -field Close

Closes an operation handle. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>.

### -field GetClass

Closes an operation handle. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>.

### -field GetIndication

Get the synchronous results from a subscription. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getindication">MI_Operation_GetIndication</a>.

### -field GetInstance

Gets a synchronous result for an instance operation. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a>.

### -field GetSession

Gets the session associated with an operation. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getsession">MI_Operation_GetSession</a>.
