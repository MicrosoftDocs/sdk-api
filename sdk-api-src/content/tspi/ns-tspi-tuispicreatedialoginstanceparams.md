---
UID: NS:tspi.tuispicreatedialoginstanceparams_tag
title: TUISPICREATEDIALOGINSTANCEPARAMS (tspi.h)
description: The TUISPI data structure is defined below.
helpviewer_keywords: ["*LPTUISPICREATEDIALOGINSTANCEPARAMS","LPTUISPICREATEDIALOGINSTANCEPARAMS","LPTUISPICREATEDIALOGINSTANCEPARAMS structure pointer [TAPI 2.2]","TUISPICREATEDIALOGINSTANCEPARAMS","TUISPICREATEDIALOGINSTANCEPARAMS structure [TAPI 2.2]","_tspi_tuispicreatedialoginstanceparams_str","tspi.tuispicreatedialoginstanceparams_str","tspi/LPTUISPICREATEDIALOGINSTANCEPARAMS","tspi/TUISPICREATEDIALOGINSTANCEPARAMS"]
old-location: tspi\tuispicreatedialoginstanceparams_str.htm
tech.root: tapi3
ms.assetid: 4de0ee9b-0643-4eab-b100-ee7aaa0b6992
ms.date: 12/05/2018
ms.keywords: '*LPTUISPICREATEDIALOGINSTANCEPARAMS, LPTUISPICREATEDIALOGINSTANCEPARAMS, LPTUISPICREATEDIALOGINSTANCEPARAMS structure pointer [TAPI 2.2], TUISPICREATEDIALOGINSTANCEPARAMS, TUISPICREATEDIALOGINSTANCEPARAMS structure [TAPI 2.2], _tspi_tuispicreatedialoginstanceparams_str, tspi.tuispicreatedialoginstanceparams_str, tspi/LPTUISPICREATEDIALOGINSTANCEPARAMS, tspi/TUISPICREATEDIALOGINSTANCEPARAMS'
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
req.typenames: TUISPICREATEDIALOGINSTANCEPARAMS, *LPTUISPICREATEDIALOGINSTANCEPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tuispicreatedialoginstanceparams_tag
 - tspi/tuispicreatedialoginstanceparams_tag
 - LPTUISPICREATEDIALOGINSTANCEPARAMS
 - tspi/LPTUISPICREATEDIALOGINSTANCEPARAMS
 - TUISPICREATEDIALOGINSTANCEPARAMS
 - tspi/TUISPICREATEDIALOGINSTANCEPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tspi.h
api_name:
 - TUISPICREATEDIALOGINSTANCEPARAMS
---

# TUISPICREATEDIALOGINSTANCEPARAMS structure


## -description

Defines parameters for TAPI dialog operations.

## -struct-fields

### -field dwRequestID

The <b>dwRequestID</b> passed to the service provider as a parameter in the asynchronous TSPI function with which the spontaneous UI is associated. TAPI uses this to identify the application in whose context the UI DLL is to be loaded and the 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialog">TUISPI_providerGenericDialog</a> function invoked.

### -field hdDlgInst

The service provider's identifier for the association with the instance of the generic dialog box. Because it is possible for multiple instances of the generic dialog box to be open in the same or multiple applications, the service provider must ensure that its handle is unique within the scope of existing instances within the context of the provider.

### -field htDlgInst

TAPI writes into this member its identifier for the association that is created. This member is set to <b>NULL</b> if creating the association failed, in which case it is impossible for the service provider to create a dialog box spontaneously in the context of the target application. The service provider must use this identifier in messages to send data to the UI DLL (<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a>).

### -field lpszUIDLLName

Pointer to a <b>NULL</b>-terminated string specifying the fully qualified name of the UI DLL to load in the application context.

### -field lpParams

Pointer to a private parameter block to be conveyed to the UI DLL's 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialog">TUISPI_providerGenericDialog</a> function. The service provider and UI DLL determine the contents of the parameter block. The transfer is unidirectional; the UI DLL is not able to modify the parameter block and return it to the service provider. Generally, this block instructs the UI DLL which dialog box to display, and contains the information to display (if necessary).

### -field dwSize

The size, in bytes, of the parameter block.

## -see-also

<a href="/windows/desktop/Tapi/line-senddialoginstancedata">LINE_SENDDIALOGINSTANCEDATA</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialog">TUISPI_providerGenericDialog</a>