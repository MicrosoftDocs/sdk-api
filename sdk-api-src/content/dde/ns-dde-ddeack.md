---
UID: NS:dde.DDEACK
title: DDEACK
author: windows-sdk-content
description: Contains status flags that a DDE application passes to its partner as part of the WM_DDE_ACK message.
old-location: dataxchg\ddeack.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangestructures\ddeack.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DDEACK, DDEACK structure [Data Exchange], _win32_DDEACK_str, _win32_ddeack_str_cpp, dataxchg.ddeack, dde/DDEACK, winui._win32_ddeack_str
ms.prod: windows-hardware
ms.technology: windows-devices
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


Contains status flags that a DDE application passes to its partner as part of the <a href="https://msdn.microsoft.com/en-us/library/ms648782(v=VS.85).aspx">WM_DDE_ACK</a> message. The flags provide details about the application's response to the messages <a href="https://msdn.microsoft.com/en-us/library/ms648994(v=VS.85).aspx">WM_DDE_DATA</a>, <a href="https://msdn.microsoft.com/en-us/library/ms648997(v=VS.85).aspx">WM_DDE_POKE</a>, <a href="https://msdn.microsoft.com/en-us/library/ms648995(v=VS.85).aspx">WM_DDE_EXECUTE</a>, <a href="https://msdn.microsoft.com/en-us/library/ms648993(v=VS.85).aspx">WM_DDE_ADVISE</a>, <a href="https://msdn.microsoft.com/en-us/library/ms649002(v=VS.85).aspx">WM_DDE_UNADVISE</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms648998(v=VS.85).aspx">WM_DDE_REQUEST</a>. 


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




<a href="https://msdn.microsoft.com/en-us/library/ms648774(v=VS.85).aspx">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648782(v=VS.85).aspx">WM_DDE_ACK</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648993(v=VS.85).aspx">WM_DDE_ADVISE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648994(v=VS.85).aspx">WM_DDE_DATA</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648995(v=VS.85).aspx">WM_DDE_EXECUTE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648997(v=VS.85).aspx">WM_DDE_POKE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648998(v=VS.85).aspx">WM_DDE_REQUEST</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649002(v=VS.85).aspx">WM_DDE_UNADVISE</a>
 

 

