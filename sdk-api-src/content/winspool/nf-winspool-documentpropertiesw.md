---
UID: NF:winspool.DocumentPropertiesW
title: DocumentPropertiesW function
author: windows-driver-content
description: The DocumentProperties function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.
old-location: gdi\documentproperties.htm
old-project: printdocs
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DM_IN_BUFFER, DM_IN_PROMPT, DM_OUT_BUFFER, DocumentProperties, DocumentProperties function [Windows GDI], DocumentPropertiesA, DocumentPropertiesW, _win32_DocumentProperties, gdi.documentproperties, winspool/DocumentProperties, winspool/DocumentPropertiesA, winspool/DocumentPropertiesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DocumentPropertiesW (Unicode) and DocumentPropertiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winspool.drv
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	DocumentProperties
-	DocumentPropertiesA
-	DocumentPropertiesW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DocumentPropertiesW function


## -description


The <b>DocumentProperties</b> function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.


## -parameters




### -param hWnd [in]

A handle to the parent window of the printer-configuration property sheet.


### -param hPrinter [in]

A handle to a printer object. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pDeviceName [in]

A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.


### -param pDevModeOutput [out]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that receives the printer configuration data specified by the user.


### -param pDevModeInput [in]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that the operating system uses to initialize the property sheet controls.

This parameter is only used if the <b>DM_IN_BUFFER</b> flag is set in the <i>fMode</i> parameter. If <b>DM_IN_BUFFER</b> is not set, the operating system uses the printer's default <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>.


### -param fMode [in]

The operations the function performs. If this parameter is zero, the <b>DocumentProperties</b> function returns the number of bytes required by the printer driver's <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> data structure. Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DM_IN_BUFFER"></a><a id="dm_in_buffer"></a><dl>
<dt><b>DM_IN_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Input value. Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure specified by the <i>pDevModeInput</i> parameter. The function updates the structure only for those members specified by the <b>DEVMODE</b> structure's <b>dmFields</b> member. This value is also defined as <b>DM_MODIFY</b>. In cases of conflict during the merge, the settings in the <b>DEVMODE</b> structure specified by <i>pDevModeInput</i> override the printer driver's current print settings.

</td>
</tr>
<tr>
<td width="40%"><a id="DM_IN_PROMPT"></a><a id="dm_in_prompt"></a><dl>
<dt><b>DM_IN_PROMPT</b></dt>
</dl>
</td>
<td width="60%">
Input value. The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> data structure to those values specified by the user. This value is also defined as <b>DM_PROMPT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="DM_OUT_BUFFER"></a><a id="dm_out_buffer"></a><dl>
<dt><b>DM_OUT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Output value. The function writes the printer driver's current print settings, including private data, to the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> data structure specified by the <i>pDevModeOutput</i> parameter. The caller must allocate a buffer sufficiently large to contain the information. If the bit <b>DM_OUT_BUFFER</b> sets is clear, the <i>pDevModeOutput</i> parameter can be <b>NULL</b>. This value is also defined as <b>DM_COPY</b>.

</td>
</tr>
</table>
 


## -returns



If the <i>fMode</i> parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data. Note that this buffer can be larger than a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure if the printer driver appends private data to the structure.

If the function displays the property sheet, the return value is either <b>IDOK</b> or <b>IDCANCEL</b>, depending on which button the user selects.

If the function does not display the property sheet and is successful, the return value is <b>IDOK</b>.

If the function fails, the return value is less than zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The string pointed to by the <i>pDeviceName</i> parameter can be obtained by calling the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function.

The <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version. Because of this driver dependence, it is very important for applications to query the driver for the correct size of the <b>DEVMODE</b> structure before allocating a buffer for it.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To make changes to print settings that are local to an application, an application should follow these steps:</b>

<ol>
<li>Get the number of bytes required for the full <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure by calling <b>DocumentProperties</b> and specifying zero in the <i>fMode</i> parameter.</li>
<li>Allocate memory for the full <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure.</li>
<li>Get the current printer settings by calling <b>DocumentProperties</b>. Pass a pointer to the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure allocated in Step 2 as the <i>pDevModeOutput</i> parameter and specify the <b>DM_OUT_BUFFER</b> value.</li>
<li>Modify the appropriate members of the returned <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure and indicate which members were changed by setting the corresponding bits in the <b>dmFields</b> member of the <b>DEVMODE</b>.</li>
<li>Call <b>DocumentProperties</b> and pass the modified <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure back as both the <i>pDevModeInput</i> and <i>pDevModeOutput</i> parameters and specify both the <b>DM_IN_BUFFER</b> and <b>DM_OUT_BUFFER</b> values (which are combined using the OR operator).The <b>DEVMODE</b> structure returned by the third call to <b>DocumentProperties</b> can be used as an argument in a call to the <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a> function.</li>
</ol>
To create a handle to a printer-device context using the current printer settings, you only need to call <b>DocumentProperties</b> twice, as described above. The first call gets the size of the full <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> and the second call initializes the <b>DEVMODE</b> with the current printer settings. Pass the initialized <b>DEVMODE</b> to <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a> to obtain the handle to the printer device context.




## -see-also




<a href="https://msdn.microsoft.com/29e33f34-f6ec-4989-b076-e1fef8eb5bc4">AdvancedDocumentProperties</a>



<a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a>



<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

