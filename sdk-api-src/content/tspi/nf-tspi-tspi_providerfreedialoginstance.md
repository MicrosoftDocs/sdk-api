---
UID: NF:tspi.TSPI_providerFreeDialogInstance
title: TSPI_providerFreeDialogInstance function (tspi.h)
description: The TSPI_providerFreeDialogInstance function informs the service provider that the dialog box associated with hdDlgInst has exited.
helpviewer_keywords: ["TSPI_providerFreeDialogInstance","TSPI_providerFreeDialogInstance function [TAPI 2.2]","_tspi_tspi_providerfreedialoginstance","tspi.tspi_providerfreedialoginstance","tspi/TSPI_providerFreeDialogInstance"]
old-location: tspi\tspi_providerfreedialoginstance.htm
tech.root: tapi3
ms.assetid: 0408c43f-cb80-4caf-ab28-5ece4b2e4851
ms.date: 12/05/2018
ms.keywords: TSPI_providerFreeDialogInstance, TSPI_providerFreeDialogInstance function [TAPI 2.2], _tspi_tspi_providerfreedialoginstance, tspi.tspi_providerfreedialoginstance, tspi/TSPI_providerFreeDialogInstance
req.header: tspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - TSPI_providerFreeDialogInstance
 - tspi/TSPI_providerFreeDialogInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_providerFreeDialogInstance
---

# TSPI_providerFreeDialogInstance function


## -description

The 
<b>TSPI_providerFreeDialogInstance</b> function informs the service provider that the dialog box associated with <i>hdDlgInst</i> has exited. After this function is called, the service provider should no longer send data to the dialog box using 
<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a> messages.

Implementation of this function is optional; it is needed only if the service provider generates spontaneous dialog boxes in application contexts using 
<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a>.

## -parameters

### -param hdDlgInst

The opaque identifier of the association between the service provider and the dialog box in the application's context, which was passed as the <b>hdDlgInstance</b> member in the 
<a href="/windows/desktop/api/tspi/ns-tspi-tuispicreatedialoginstanceparams">TUISPICREATEDIALOGINSTANCEPARAMS</a> structure with the LINE_CREATEDIALOGINSTANCE message that created the dialog box.

## -returns

Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a>



<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a>



<a href="/windows/desktop/api/tspi/ns-tspi-tuispicreatedialoginstanceparams">TUISPICREATEDIALOGINSTANCEPARAMS</a>