---
UID: NF:winddi.EngGetPrinterData
title: EngGetPrinterData function
author: windows-sdk-content
description: The EngGetPrinterData function retrieves configuration data for the specified printer.
old-location: display\enggetprinterdata.htm
old-project: display
ms.assetid: aeeda5d8-1447-42e4-b54b-39f657a0a53c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngGetPrinterData, EngGetPrinterData function [Display Devices], display.enggetprinterdata, gdifncs_63eb49b8-c997-4d78-b4ec-0620afac41e9.xml, winddi/EngGetPrinterData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngGetPrinterData
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngGetPrinterData function


## -description


The <b>EngGetPrinterData </b>function retrieves configuration data for the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which configuration data should be retrieved. This is the handle that is passed as the <i>hDriver</i> parameter of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param pValueName [in]

Pointer to a null-terminated string that identifies the data to be retrieved.


### -param pType [out, optional]

Pointer to a variable that receives the data type stored by <a href="https://msdn.microsoft.com/library/windows/hardware/ff565020">EngSetPrinterData</a>. This parameter can be <b>NULL</b>.


### -param pData [out, optional]

Pointer to an array of bytes in which the configuration data is written.


### -param nSize [in]

Specifies the size, in bytes, of <i>pData</i>.


### -param pcbNeeded [out]

Pointer to a memory location that receives the number of bytes copied into <i>lpbData</i> if the function succeeds. This parameter receives the number of bytes required if <i>nSizef</i> is too small.


## -returns



<b>EngGetPrinterData</b> returns the last logged error message.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565020">EngSetPrinterData</a>
 

 

