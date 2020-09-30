---
UID: NC:tspi.TUISPIDLLCALLBACK
title: TUISPIDLLCALLBACK (tspi.h)
description: The DllCallbackProc function is called by the UI DLL to send a private parameter block to the service provider.
helpviewer_keywords: ["DllCallbackProc","DllCallbackProc callback function [TAPI 2.2]","TUISPIDLLCALLBACK","TUISPIDLLCALLBACK callback","_tspi_tuispidllcallback","tspi.dllcallbackproc","tspi.tuispidllcallback","tspi/DllCallbackProc"]
old-location: tspi\dllcallbackproc.htm
tech.root: tapi3
ms.assetid: 2f4ec748-26ff-49c5-bd88-6c6e64e5bc89
ms.date: 12/05/2018
ms.keywords: DllCallbackProc, DllCallbackProc callback function [TAPI 2.2], TUISPIDLLCALLBACK, TUISPIDLLCALLBACK callback, _tspi_tuispidllcallback, tspi.dllcallbackproc, tspi.tuispidllcallback, tspi/DllCallbackProc
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
 - TUISPIDLLCALLBACK
 - tspi/TUISPIDLLCALLBACK
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
 - DllCallbackProc
---

# TUISPIDLLCALLBACK callback function


## -description

The <i>DllCallbackProc</i> 
function is called by the UI DLL to send a private parameter block to the service provider. Each invocation of the callback results in a call to the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providergenericdialogdata">TSPI_providerGenericDialogData</a> function in the service provider associated with the specified object. The contents of the parameter block are defined by the service provider and UI DLL. The service provider can modify the contents of the parameter block; when this function returns, TAPI copies the modified data back into the original UI DLL parameter block.

The <b>TUISPIDLLCALLBACK</b> type defines a pointer to this callback function. <i>DllCallbackProc</i> is a placeholder for the application-defined function name.

## -parameters

### -param dwObjectID

An object identifier of the type specified by <i>dwObjectType</i>.

### -param dwObjectType

One of the 
<a href="/windows/desktop/Tapi/tuispidll-object-">TUISPIDLL_OBJECT_</a> constants, specifying the type of object identified by <i>dwObjectID</i>





#### TUISPIDLL_OBJECT_LINEID

The <i>dwObjectID</i> parameter is a line device identifier (<i>dwDeviceID</i>). This is used when the callback is invoked during the processing of 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialog">TUISPI_lineConfigDialog</a> or 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialogedit">TUISPI_lineConfigDialogEdit</a>.



#### TUISPIDLL_OBJECT_PHONEID

The <i>dwObjectID</i> parameter is a phone device identifier (<i>dwDeviceID</i>). This is used when the callback is invoked during the processing of 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_phoneconfigdialog">TUISPI_phoneConfigDialog</a>.



#### TUISPIDLL_OBJECT_PROVIDERID

The <i>dwObjectID</i> parameter is a permanent provider identifier. This is used when the callback is invoked during the processing of 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerconfig">TUISPI_providerConfig</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerinstall">TUISPI_providerInstall</a>, or 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerremove">TUISPI_providerRemove</a>.



#### TUISPIDLL_OBJECT_DIALOGINSTANCE

The <i>dwObjectID</i> parameter is an HDRVDIALOGINSTANCE, as returned to the service provider when it sent a 
<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a> message. This is used when the callback is invoked during the processing of 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialog">TUISPI_providerGenericDialog</a>.

### -param lpParams

Pointer to a memory area used to hold a parameter block.

### -param dwSize

The size in bytes of the parameter block. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

## -returns

Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/Tapi/line-createdialoginstance">LINE_CREATEDIALOGINSTANCE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providergenericdialogdata">TSPI_providerGenericDialogData</a>



<a href="/windows/desktop/Tapi/tuispidll-object-">TUISPIDLL_OBJECT_</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialog">TUISPI_lineConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialogedit">TUISPI_lineConfigDialogEdit</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_phoneconfigdialog">TUISPI_phoneConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerconfig">TUISPI_providerConfig</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providergenericdialog">TUISPI_providerGenericDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerinstall">TUISPI_providerInstall</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerremove">TUISPI_providerRemove</a>