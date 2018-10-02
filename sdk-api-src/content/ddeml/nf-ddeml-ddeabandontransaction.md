---
UID: NF:ddeml.DdeAbandonTransaction
title: DdeAbandonTransaction function
author: windows-sdk-content
description: Abandons the specified asynchronous transaction and releases all resources associated with the transaction.
old-location: dataxchg\ddeabandontransaction.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeabandontransaction.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DdeAbandonTransaction, DdeAbandonTransaction function [Data Exchange], _win32_DdeAbandonTransaction, _win32_ddeabandontransaction_cpp, dataxchg.ddeabandontransaction, ddeml/DdeAbandonTransaction, winui._win32_ddeabandontransaction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ddeml.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeAbandonTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeAbandonTransaction function


## -description


Abandons the specified asynchronous transaction and releases all resources associated with the transaction. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation in which the transaction was initiated. If this parameter is 0L, all transactions are abandoned (that is, the 
					<i>idTransaction</i> parameter is ignored). 


### -param idTransaction [in]

Type: <b>DWORD</b>

The identifier of the transaction to be abandoned. If this parameter is 0L, all active transactions in the specified conversation are abandoned. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



Only a Dynamic Data Exchange (DDE) client application should call <b>DdeAbandonTransaction</b>. If the server application responds to the transaction after the client has called <b>DdeAbandonTransaction</b>, the system discards the transaction results. This function has no effect on synchronous transactions. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/024655dd-f4de-4aad-a6fe-81e8322e228e">DdeClientTransaction</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

