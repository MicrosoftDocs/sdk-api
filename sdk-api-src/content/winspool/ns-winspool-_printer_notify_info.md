---
UID: NS:winspool._PRINTER_NOTIFY_INFO
title: "_PRINTER_NOTIFY_INFO"
author: windows-driver-content
description: The PRINTER_NOTIFY_INFO structure contains printer information returned by the FindNextPrinterChangeNotification function. The function returns this information after a wait operation on a printer change notification object has been satisfied.
old-location: gdi\printer_notify_info.htm
old-project: printdocs
ms.assetid: c104fabe-edf5-426e-859b-694811975623
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO, PPRINTER_NOTIFY_INFO, PPRINTER_NOTIFY_INFO structure pointer [Windows GDI], PRINTER_NOTIFY_INFO, PRINTER_NOTIFY_INFO structure [Windows GDI], _PRINTER_NOTIFY_INFO, _win32_PRINTER_NOTIFY_INFO_str, gdi.printer_notify_info, winspool/PPRINTER_NOTIFY_INFO, winspool/PRINTER_NOTIFY_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
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
req.typenames: PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO, *LPPRINTER_NOTIFY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_NOTIFY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_NOTIFY_INFO structure


## -description



The <b>PRINTER_NOTIFY_INFO</b> structure contains printer information returned by the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function. The function returns this information after a wait operation on a printer change notification object has been satisfied.




## -struct-fields




### -field Version

The version of this structure. Set this member to 2.


### -field Flags

A bit flag that indicates the state of the notification structure. If the PRINTER_NOTIFY_INFO_DISCARDED bit is set, it indicates that some notifications had to be discarded.


### -field Count

The number of <a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a> elements in the <b>aData</b> array.


### -field aData

An array of <a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a> structures. Each element of the array identifies a single job or printer information field, and provides the current data for that field.


## -remarks



If the <b>Flags</b> member has the PRINTER_NOTIFY_INFO_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost. In this case, you must call <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> and specify the PRINTER_NOTIFY_OPTIONS_REFRESH flag to retrieve all current information. Until you request this refresh operation, the system will not send additional notifications for this change notification object.




## -see-also




<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

