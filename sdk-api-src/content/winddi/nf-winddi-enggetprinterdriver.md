---
UID: NF:winddi.EngGetPrinterDriver
title: EngGetPrinterDriver function
author: windows-sdk-content
description: The EngGetPrinterDriver function retrieves driver data for the specified printer.
old-location: display\enggetprinterdriver.htm
old-project: display
ms.assetid: baf6826f-511d-4820-9990-be82ceba23fe
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngGetPrinterDriver, EngGetPrinterDriver function [Display Devices], display.enggetprinterdriver, gdifncs_0aead020-6bf8-4eda-8d72-dd2d59f4663d.xml, winddi/EngGetPrinterDriver
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngGetPrinterDriver
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngGetPrinterDriver function


## -description


The <b>EngGetPrinterDriver</b> function retrieves driver data for the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which the driver data should be retrieved.


### -param pEnvironment [in, optional]

Pointer to a null-terminated string that specifies the environment. For example, "Windows NT x86" specifies an NT-based operating system running on an Intel processor. If <i>pEnvironment</i> is <b>NULL</b>, the current environment of the calling driver and client machine is used.


### -param dwLevel [in]

Specifies the version of the structure to which <i>lpbDrvInfo</i> points. This parameter must be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
1

</td>
<td>
GDI writes a DRIVER_INFO_1 structure in the buffer to which <i>lpbDrvInfo</i> points.

</td>
</tr>
<tr>
<td>
2

</td>
<td>
GDI writes a DRIVER_INFO_2 structure in the buffer to which <i>lpbDrvInfo</i> points.

</td>
</tr>
<tr>
<td>
3

</td>
<td>
GDI writes a DRIVER_INFO_3 structure in the buffer to which <i>lpbDrvInfo</i> points.

</td>
</tr>
</table>
 


### -param lpbDrvInfo [out, optional]

Pointer to a buffer in which GDI places the requested DRIVER_INFO_<i>X</i> structure.


### -param cbBuf [in]

Specifies the size, in bytes, of the buffer to which <i>lpbDrvInfo</i> points.


### -param pcbNeeded [out]

Pointer to a memory location in which GDI places the number of bytes copied into the buffer to which <i>lpbDrvInfo</i> points upon success, or the number of bytes required if <i>cbBuf</i> is too small.


## -returns



<b>EngGetPrinterDriver</b> returns <b>TRUE</b> upon success; otherwise it reports an error and returns <b>FALSE</b>.




## -remarks



A printer driver DLL can work with multiple data files to support different printer models. The printer driver calls <b>EngGetPrinterDriver</b> to determine which data file to use. For example, the Unidrv renderer calls this function to determine the name of a <a href="https://msdn.microsoft.com/f67c673d-c6f0-49f0-850a-d8b00e99ddd4">GPD</a> file, and the postscript driver calls this function to determine the name of a <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PPD</a> file. The DRIVER_INFO_2 and DRIVER_INFO_3 structures contain a full path and file name specifying the location of the data file. The printer driver can then use the returned path and file name to load the data file by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a> with the path and file name as a single argument.

The DRIVER_INFO_<i>X</i> structures are described in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>
 

 

