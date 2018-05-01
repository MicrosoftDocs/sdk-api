---
UID: NF:wiamicro.Scan
title: Scan function
author: windows-driver-content
description: The Scan function reads data from the device and returns the data to the WIA Flatbed driver.
old-location: image\scan.htm
old-project: image
ms.assetid: 057b548a-d9e4-4db4-b34f-d867b7be3971
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: MicroDrv_ab289619-86b7-47fd-a5f5-e8533da4db31.xml, Scan, Scan function [Imaging Devices], image.scan, wiamicro/Scan
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamicro.h
req.include-header: Wiamicro.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	Scan
product: Windows
targetos: Windows
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: 
req.product: Windows Address Book 5.0
---

# Scan function


## -description


The <b>Scan</b> function reads data from the device and returns the data to the WIA Flatbed driver. 


## -parameters




### -param pScanInfo [in, out]

Specifies the <a href="https://msdn.microsoft.com/library/windows/hardware/ff547361">SCANINFO</a> structure that represents the microdriver's settings. This is stored by the WIA Flatbed driver to guarantee that the settings between the microdriver and the WIA Flatbed driver are synchronized. 


### -param lPhase

Specifies the scan phase requested. This parameter can be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SCAN_FIRST

</td>
<td>
This signals the first phase of the scan. The microdriver performs three tasks: it initializes the device, it uses the data in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff547361">SCANINFO</a> structure to set up the scan (for example, set the resolution, the start position, the width and the height on the device), and it starts the scan. Data must be returned from this call. Data must be put into the buffer pointed to by <i>pBuffer</i> and the <i>pReceived</i> parameter must be set to the amount of data put in the buffer.

</td>
</tr>
<tr>
<td>
SCAN_NEXT

</td>
<td>
This will be repeatedly called during the data transfer. Data should be put into the buffer pointed to by <i>pBuffer</i> and the <i>pReceived</i> parameter must be set to the amount of data put in the buffer.

</td>
</tr>
<tr>
<td>
SCAN_FINISHED

</td>
<td>
This will be called at the end of the scan to terminate the scanning process. No data should be transferred. SCAN_FINISHED will always be called even if the user cancels the scan. The microdriver should stop transferring data and the scanner should be reset so that it is ready for the next scan.

The data returned from this function should be in raw format without any header. The data can be either packed or planar, aligned or unaligned, and in RGB or BGR order. Set the <b>RawDataFormat</b>, <b>RawPixelOrder</b>, and <b>bNeedDataAlignment</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff547361">SCANINFO</a> structure appropriately in response to the CMD_INITIALIZE command.

</td>
</tr>
</table>
 


### -param pBuffer [out]

Specifies the buffer that will be filled with scanned data by the microdriver. This buffer is allocated by the WIA Flatbed Driver and is guaranteed to be at least <i>lLength</i> bytes in length.


### -param lLength

Specifies the requested amount of data that will be scanned. The microdriver must never overfill the buffer pointed to by <i>pBuffer</i>.


### -param plReceived

TBD




#### - pReceived [out]

Specifies the amount of data actually scanned into <i>pBuffer</i>. This value should never exceed the value of <i>lLength</i>, but can be less.


## -returns



If the function succeeds, it returns S_OK. If the function fails, it returns a standard COM error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547361">SCANINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552714">WIA Microdriver Commands</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552722">WIA Microdriver Structures</a>
 

 

