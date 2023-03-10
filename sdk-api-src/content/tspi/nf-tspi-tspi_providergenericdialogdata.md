---
UID: NF:tspi.TSPI_providerGenericDialogData
title: TSPI_providerGenericDialogData function (tspi.h)
description: The TSPI_providerGenericDialogData function delivers to the service provider data that was sent from the UI DLL running in an application context through the TUISPIDLLCALLBACK function.
helpviewer_keywords: ["TSPI_providerGenericDialogData","TSPI_providerGenericDialogData function [TAPI 2.2]","_tspi_tspi_providergenericdialogdata","tspi.tspi_providergenericdialogdata","tspi/TSPI_providerGenericDialogData"]
old-location: tspi\tspi_providergenericdialogdata.htm
tech.root: tapi3
ms.assetid: f48d1995-c775-4ae6-9af8-5f5f5c4f4ebe
ms.date: 12/05/2018
ms.keywords: TSPI_providerGenericDialogData, TSPI_providerGenericDialogData function [TAPI 2.2], _tspi_tspi_providergenericdialogdata, tspi.tspi_providergenericdialogdata, tspi/TSPI_providerGenericDialogData
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
 - TSPI_providerGenericDialogData
 - tspi/TSPI_providerGenericDialogData
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
 - TSPI_providerGenericDialogData
---

# TSPI_providerGenericDialogData function


## -description

The 
<b>TSPI_providerGenericDialogData</b> function delivers to the service provider data that was sent from the UI DLL running in an application context through the 
<a href="/windows/desktop/api/tspi/nc-tspi-tuispidllcallback">TUISPIDLLCALLBACK</a> function. The contents of the memory block pointed to by <i>lpParams</i> is defined by the service provider and UI DLL. The service provider can modify the contents of the parameter block; when this function returns, TAPI copies the modified data back into the original UI DLL parameter block.

Implementation is mandatory if the UI DLL associated with the service provider calls 
<a href="/windows/desktop/api/tspi/nc-tspi-tuispidllcallback">TUISPIDLLCALLBACK</a>.

## -parameters

### -param dwObjectID

An object identifier of the type specified by <i>dwObjectType</i>.

### -param dwObjectType

One of the 
<a href="/windows/desktop/Tapi/tuispidll-object-">TUISPIDLL_OBJECT_</a> constants, specifying the type of object identified by <i>dwObjectID</i>:





#### TUISPIDLL_OBJECT_LINEID

<i>dwObjectID</i> is a line device identifier (dwDeviceID).



#### TUISPIDLL_OBJECT_PHONEID

<i>dwObjectID</i> is a phone device identifier (dwDeviceID)



#### TUISPIDLL_OBJECT_PROVIDERID

<i>dwObjectID</i> is a permanent provider identifier.



#### TUISPIDLL_OBJECT_DIALOGINSTANCE

<i>dwObjectID</i> is an HDRVDIALOGINSTANCE, as returned to the service provider when it sent a 
<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a> message.

### -param lpParams

Pointer to a memory area used to hold a parameter block. The contents of this parameter block are specific to the service provider and its associated UI DLL.

### -param dwSize

The size in bytes of the parameter block. If the <i>lpParams</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.

## -returns

Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a>



<a href="/windows/desktop/api/tspi/nc-tspi-tuispidllcallback">TUISPIDLLCALLBACK</a>