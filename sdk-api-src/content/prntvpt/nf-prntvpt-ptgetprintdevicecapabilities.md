---
UID: NF:prntvpt.PTGetPrintDeviceCapabilities
title: PTGetPrintDeviceCapabilities function
author: windows-sdk-content
description: Retrieves the device printer's capabilities formatted in compliance with the XML Print Schema.
old-location: xps\ptgetprintdevicecapabilities.htm
tech.root: printdocs
ms.assetid: DB9D63B1-2703-47F7-8F31-30FA0110E1E9
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: PTGetPrintDeviceCapabilities, PTGetPrintDeviceCapabilities function [XPS Documents and Packaging], prntvpt/PTGetPrintDeviceCapabilities, xps.ptgetprintdevicecapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: prntvpt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - prntvpt.dll
api_name:
 - PTGetPrintDeviceCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PTGetPrintDeviceCapabilities function


## -description


Retrieves the device printer's capabilities formatted in compliance with the XML <a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a>.


## -parameters




### -param hProvider [in]

A handle to an open device provider whose print capabilities are to be retrieved. This handle is returned by the <a href="https://msdn.microsoft.com/6821b1b0-74b0-4caf-b8e6-a9df4d7693d7">PTOpenProvider</a> or the <a href="https://msdn.microsoft.com/0e65170b-66f6-4238-bdde-0a0b7108a686">PTOpenProviderEx</a> function.


### -param pPrintTicket [in, optional]

An optional pointer to a stream with its seek position at the beginning of the print ticket content. This parameter can be <b>NULL</b>.


### -param pDeviceCapabilities

A pointer to the stream where the device print capabilities will be written, starting at the current seek position.


### -param pbstrErrorMessage [out, optional]

A pointer to a PDC file or string that specifies what, if anything, is invalid about <i>pPrintTicket</i>. If it is valid, this value is <b>NULL</b>.The function uses this parameter only used if <i>pPrintTicket</i> is used.


## -returns



If the operation succeeds, the return value is S_OK. Otherwise, returns an error message.




## -see-also




<a href="https://msdn.microsoft.com/925e314c-85ff-4c1b-b3c9-f36aa4b55e01">PTGetPrintCapabilities</a>
 

 

