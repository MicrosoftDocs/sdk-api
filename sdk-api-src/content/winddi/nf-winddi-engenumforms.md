---
UID: NF:winddi.EngEnumForms
title: EngEnumForms function
author: windows-driver-content
description: The EngEnumForms function enumerates the forms supported by the specified printer.
old-location: display\engenumforms.htm
old-project: display
ms.assetid: c249bb86-52cf-4c9d-9ea2-7e3a7d14a31a
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: EngEnumForms, EngEnumForms function [Display Devices], display.engenumforms, gdifncs_62f2ba18-75e2-4636-94cf-c4a0b2b63ab1.xml, winddi/EngEnumForms
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	EngEnumForms
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngEnumForms function


## -description


The <b>EngEnumForms</b> function enumerates the forms supported by the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which the forms should be enumerated. This is the PDEV handle that is passed as the <i>hDriver</i> parameter of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param Level [in]

Specifies the version of the structure pointed to by <i>pForm</i>. This value must be 1, which indicates that the enumerated forms are to be returned in FORM_1_INFO structures.


### -param pForm [out, optional]

Pointer to an array of bytes in which the enumerated FORM_INFO_1 structures are written.


### -param cbBuf [in]

Specifies the size, in bytes, of <i>lpbForms</i>.


### -param pcbNeeded [out]

Pointer to a DWORD that receives the number of bytes copied into <i>pForm </i>if the copy is completed successfully. If <i>pForm</i> is too small to contain all the enumerated forms' data, this DWORD specifies the number of bytes required.


### -param pcReturned [out]

Pointer to a DWORD that receives the number of FORM_INFO_1 structures copied into <i>pForm</i>.


## -returns



<b>EngEnumForms</b> returns <b>TRUE</b> if all parameters are valid and the enumerated form data is successfully copied into <i>pForm</i>. Otherwise, it returns <b>FALSE</b> and an error message is logged. To get error information, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>.




## -remarks



A printer driver can call <b>EngEnumForms</b> to have GDI obtain the list of forms supported by a particular printer. The enumerated information is returned as an array of FORM_INFO_1 structures (declared in the Microsoft Windows SDK documentation) pointed to by <i>pForm</i>. If the array pointed to by <i>pForm</i> is not large enough to hold the enumerated data, the requisite array size is instead returned in <i>pcbNeeded</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>
 

 

