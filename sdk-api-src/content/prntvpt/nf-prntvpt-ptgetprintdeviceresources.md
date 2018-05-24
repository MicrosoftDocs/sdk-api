---
UID: NF:prntvpt.PTGetPrintDeviceResources
title: PTGetPrintDeviceResources function
author: windows-driver-content
description: It retrieves the print devices resources for a printer formatted in compliance with the XML Print Schema.
old-location: xps\ptgetprintdeviceresources.htm
old-project: printdocs
ms.assetid: 39F17562-B8EB-41AF-BA55-42FE35B4560F
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PTGetPrintDeviceResources, PTGetPrintDeviceResources function [XPS Documents and Packaging], prntvpt/PTGetPrintDeviceResources, xps.ptgetprintdeviceresources
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
req.typenames: EDefaultDevmodeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	prntvpt.dll
api_name:
-	PTGetPrintDeviceResources
product: Windows
targetos: Windows
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PTGetPrintDeviceResources function


## -description


It retrieves the print devices resources for a printer formatted in compliance with the XML <a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a>.


## -parameters




### -param hProvider [in]

A handle to an open device provider whose print device resources are to be retrieved. This handle is returned by the <a href="https://msdn.microsoft.com/6821b1b0-74b0-4caf-b8e6-a9df4d7693d7">PTOpenProvider</a> or the <a href="https://msdn.microsoft.com/0e65170b-66f6-4238-bdde-0a0b7108a686">PTOpenProviderEx</a> function.


### -param pszLocaleName

TBD


### -param pPrintTicket [in]

A pointer to a stream with its seek position at the beginning of the print ticket content. This parameter can be <b>NULL</b>.


### -param pDeviceResources

A pointer to the stream where the device print resources will be written, starting at the current seek position.


### -param pbstrErrorMessage [out, optional]

A pointer to a PDC file or string that specifies what, if anything, is invalid about <i>pPrintTicket</i>. If it is valid, this value is <b>NULL</b>.


#### - pzLocaleName [in]

Optional pointer to the locale name. This parameter can be <b>NULL</b>.


## -returns



If the operation succeeds, the return value is S_OK. Otherwise, returns an error message. 




## -see-also




<a href="https://msdn.microsoft.com/925e314c-85ff-4c1b-b3c9-f36aa4b55e01">PTGetPrintCapabilities</a>



<a href="https://msdn.microsoft.com/DB9D63B1-2703-47F7-8F31-30FA0110E1E9">PTGetPrintDeviceCapabilities</a>
 

 

