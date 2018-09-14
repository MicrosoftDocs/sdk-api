---
UID: NS:dde.DDEACK
title: DDEACK
author: windows-sdk-content
description: Contains status flags that a DDE application passes to its partner as part of the WM_DDE_ACK message.
old-location: dataxchg\ddeack.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangestructures\ddeack.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DDEACK, DDEACK structure [Data Exchange], _win32_DDEACK_str, _win32_ddeack_str_cpp, dataxchg.ddeack, dde/DDEACK, winui._win32_ddeack_str
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dde.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dde.h
api_name:
 - DDEACK
product: Windows
targetos: Windows
req.typenames: DDEACK
req.redist: 
---

# DDEACK structure


## -description


Contains status flags that a DDE application passes to its partner as part of the <a href="https://msdn.microsoft.com/aca47dbf-e1f2-4725-8364-0aa7fcd98bd9">WM_DDE_ACK</a> message. The flags provide details about the application's response to the messages <a href="https://msdn.microsoft.com/ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a">WM_DDE_DATA</a>, <a href="https://msdn.microsoft.com/848142b7-a7ef-4206-9bb3-b511388cfaaa">WM_DDE_POKE</a>, <a href="https://msdn.microsoft.com/23c18a57-83ee-4fd3-a5bc-71645bda34eb">WM_DDE_EXECUTE</a>, <a href="https://msdn.microsoft.com/b00db740-36a7-4487-abbf-d74b12f5212a">WM_DDE_ADVISE</a>, <a href="https://msdn.microsoft.com/9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1">WM_DDE_UNADVISE</a>, and <a href="https://msdn.microsoft.com/922452d2-455c-43e1-a8a8-e3c52b0fab51">WM_DDE_REQUEST</a>. 


## -struct-fields




### -field bAppReturnCode

Type: <b>unsigned short</b>

An application-defined return code. 


### -field reserved

Type: <b>unsigned short</b>

Reserved. 


### -field fBusy

Type: <b>unsigned short</b>

Indicates whether the application was busy and unable to respond to the partner's message at the time the message was received. A nonzero value indicates the partner was busy and unable to respond. The <b>fBusy</b> member is defined only when the <b>fAck</b> member is zero. 


### -field fAck

Type: <b>unsigned short</b>

Indicates whether the application accepted the message from its partner. A nonzero value indicates the partner accepted the message. 


### -field usFlags

 




## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/aca47dbf-e1f2-4725-8364-0aa7fcd98bd9">WM_DDE_ACK</a>



<a href="https://msdn.microsoft.com/b00db740-36a7-4487-abbf-d74b12f5212a">WM_DDE_ADVISE</a>



<a href="https://msdn.microsoft.com/ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a">WM_DDE_DATA</a>



<a href="https://msdn.microsoft.com/23c18a57-83ee-4fd3-a5bc-71645bda34eb">WM_DDE_EXECUTE</a>



<a href="https://msdn.microsoft.com/848142b7-a7ef-4206-9bb3-b511388cfaaa">WM_DDE_POKE</a>



<a href="https://msdn.microsoft.com/922452d2-455c-43e1-a8a8-e3c52b0fab51">WM_DDE_REQUEST</a>



<a href="https://msdn.microsoft.com/9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1">WM_DDE_UNADVISE</a>
 

 

