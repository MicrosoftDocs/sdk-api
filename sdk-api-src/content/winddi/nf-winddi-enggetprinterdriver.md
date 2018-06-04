---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

