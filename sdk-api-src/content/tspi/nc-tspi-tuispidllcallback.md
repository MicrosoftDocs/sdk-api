---
UID: NC:tspi.TUISPIDLLCALLBACK
title: TUISPIDLLCALLBACK
author: windows-sdk-content
description: The DllCallbackProc function is called by the UI DLL to send a private parameter block to the service provider.
old-location: tspi\dllcallbackproc.htm
old-project: tapi
ms.assetid: 2f4ec748-26ff-49c5-bd88-6c6e64e5bc89
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DllCallbackProc, DllCallbackProc callback function [TAPI 2.2], TUISPIDLLCALLBACK, TUISPIDLLCALLBACK callback, _tspi_tuispidllcallback, tspi.dllcallbackproc, tspi.tuispidllcallback, tspi/DllCallbackProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - DllCallbackProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TUISPIDLLCALLBACK callback function


## -description


The <i>DllCallbackProc</i> 
function is called by the UI DLL to send a private parameter block to the service provider. Each invocation of the callback results in a call to the 
<a href="https://msdn.microsoft.com/f48d1995-c775-4ae6-9af8-5f5f5c4f4ebe">TSPI_providerGenericDialogData</a> function in the service provider associated with the specified object. The contents of the parameter block are defined by the service provider and UI DLL. The service provider can modify the contents of the parameter block; when this function returns, TAPI copies the modified data back into the original UI DLL parameter block.

The <b>TUISPIDLLCALLBACK</b> type defines a pointer to this callback function. <i>DllCallbackProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param dwObjectID

An object identifier of the type specified by <i>dwObjectType</i>.


### -param dwObjectType

One of the 
<a href="https://msdn.microsoft.com/bc0f876d-2443-4c3c-b723-3f82dc6bf849">TUISPIDLL_OBJECT_</a> constants, specifying the type of object identified by <i>dwObjectID</i>





#### TUISPIDLL_OBJECT_LINEID

The <i>dwObjectID</i> parameter is a line device identifier (<i>dwDeviceID</i>). This is used when the callback is invoked during the processing of 
<a href="https://msdn.microsoft.com/405af7aa-eb0b-49a1-9712-2f86357fc720">TUISPI_lineConfigDialog</a> or 
<a href="https://msdn.microsoft.com/05169974-31f3-445b-b55f-5931bace6505">TUISPI_lineConfigDialogEdit</a>.



#### TUISPIDLL_OBJECT_PHONEID

The <i>dwObjectID</i> parameter is a phone device identifier (<i>dwDeviceID</i>). This is used when the callback is invoked during the processing of 
<a href="https://msdn.microsoft.com/6bdd4206-0028-43f0-8da8-2fc11779f7d2">TUISPI_phoneConfigDialog</a>.



#### TUISPIDLL_OBJECT_PROVIDERID

The <i>dwObjectID</i> parameter is a permanent provider identifier. This is used when the callback is invoked during the processing of 
<a href="https://msdn.microsoft.com/9730f61a-8da7-4693-9fd2-94650e36ce8a">TUISPI_providerConfig</a>, 
<a href="https://msdn.microsoft.com/4b133336-7cd1-4af4-bc8d-4defce97559d">TUISPI_providerInstall</a>, or 
<a href="https://msdn.microsoft.com/217d1f40-7f3f-49a0-b29e-e2da85ba47f1">TUISPI_providerRemove</a>.



#### TUISPIDLL_OBJECT_DIALOGINSTANCE

The <i>dwObjectID</i> parameter is an HDRVDIALOGINSTANCE, as returned to the service provider when it sent a 
<a href="https://msdn.microsoft.com/5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75">LINE_CREATEDIALOGINSTANCE</a> message. This is used when the callback is invoked during the processing of 
<a href="https://msdn.microsoft.com/2615ad41-b9bb-4bd4-9cfa-26b3c3336bee">TUISPI_providerGenericDialog</a>.


### -param lpParams

Pointer to a memory area used to hold a parameter block.


### -param dwSize

The size in bytes of the parameter block. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

## -returns



Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.




## -see-also




<a href="https://msdn.microsoft.com/5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75">LINE_CREATEDIALOGINSTANCE</a>



<a href="https://msdn.microsoft.com/f48d1995-c775-4ae6-9af8-5f5f5c4f4ebe">TSPI_providerGenericDialogData</a>



<a href="https://msdn.microsoft.com/bc0f876d-2443-4c3c-b723-3f82dc6bf849">TUISPIDLL_OBJECT_</a>



<a href="https://msdn.microsoft.com/405af7aa-eb0b-49a1-9712-2f86357fc720">TUISPI_lineConfigDialog</a>



<a href="https://msdn.microsoft.com/05169974-31f3-445b-b55f-5931bace6505">TUISPI_lineConfigDialogEdit</a>



<a href="https://msdn.microsoft.com/6bdd4206-0028-43f0-8da8-2fc11779f7d2">TUISPI_phoneConfigDialog</a>



<a href="https://msdn.microsoft.com/9730f61a-8da7-4693-9fd2-94650e36ce8a">TUISPI_providerConfig</a>



<a href="https://msdn.microsoft.com/2615ad41-b9bb-4bd4-9cfa-26b3c3336bee">TUISPI_providerGenericDialog</a>



<a href="https://msdn.microsoft.com/4b133336-7cd1-4af4-bc8d-4defce97559d">TUISPI_providerInstall</a>



<a href="https://msdn.microsoft.com/217d1f40-7f3f-49a0-b29e-e2da85ba47f1">TUISPI_providerRemove</a>
 

 

