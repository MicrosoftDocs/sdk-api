---
UID: NF:wingdi.ExtEscape
title: ExtEscape function
author: windows-driver-content
description: The CHECKJPEGFORMAT printer escape function determines whether a printer supports printing a JPEG image.
old-location: gdi\checkjpegformat.htm
old-project: printdocs
ms.assetid: 7af01433-36e7-494e-80ee-cbf54fce4019
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CHECKJPEGFORMAT, CHECKJPEGFORMAT Printer Escape, ExtEscape, ExtEscape function [Windows GDI], _win32_CHECKJPEGFORMAT, gdi.checkjpegformat, wingdi/ExtEscape
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	ExtEscape
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ExtEscape function


## -description


The <b>CHECKJPEGFORMAT</b> printer escape function determines whether a printer supports printing a JPEG image.

To perform this check, call the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function with the following parameters.


## -parameters




### -param hdc [in]

A handle to the printer device context.


### -param iEscape

TBD


### -param cjInput

TBD


### -param lpInData

TBD


### -param cjOutput

TBD


### -param lpOutData

TBD




#### - cbInput [in]

The size, in bytes, of the JPEG image buffer pointed to by the <i>lpszInData</i> parameter.


#### - cbOutput [in]

The number of bytes of data pointed to by the <i>lpszOutData</i> parameter.

For this escape, set this value to <code>sizeof ( DWORD )</code>.


#### - lpszInData [in]

A pointer to a buffer that contains the JPEG image.


#### - lpszOutData [out]

A pointer to the <b>DWORD</b> variable that receives the output from this escape. This parameter must not be <b>NULL</b>.

 If the printer supports the image type, this value is set to 1. Otherwise, it is set to zero.


#### - nEscape [in]

The escape function to be performed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHECKJPEGFORMAT"></a><a id="checkjpegformat"></a><dl>
<dt><b><b>CHECKJPEGFORMAT</b></b></dt>
</dl>
</td>
<td width="60%">
Checks whether the printer supports printing a JPEG image.

</td>
</tr>
</table>
 


## -returns



The return value is greater than zero if the function is successful and less than zero if not. A return value of zero indicates that the printer does not support this escape.




## -remarks



Before using the <b>CHECKJPEGFORMAT</b> printer escape function, call the <a href="https://msdn.microsoft.com/25aaf9da-50ec-4fde-af93-aa2c03a74d6d">QUERYESCSUPPORT</a> printer escape function to determine whether the driver supports <b>CHECKJPEGFORMAT</b>. For sample code that demonstrates the use of <b>CHECKJPEGFORMAT</b>, see <a href="https://msdn.microsoft.com/7cbb2b7a-2d95-4352-9e75-aa814e8f01bd">Testing a Printer for JPEG or PNG Support</a>.




## -see-also




<a href="https://msdn.microsoft.com/2714de8d-56a1-431d-a85e-7ce988d6a87b">CHECKPNGFORMAT</a>



<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/1e54b151-2324-4d6b-975a-feb42c37b18d">GDI Printer Escape Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/25aaf9da-50ec-4fde-af93-aa2c03a74d6d">QUERYESCSUPPORT</a>
 

 

