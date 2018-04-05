---
UID: NF:winspool.EnumPrintersW
title: EnumPrintersW function
author: windows-driver-content
description: The EnumPrinters function enumerates available printers, print servers, domains, or print providers.
old-location: gdi\enumprinters.htm
old-project: printdocs
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumPrinters, EnumPrinters function [Windows GDI], EnumPrintersA, EnumPrintersW, PRINTER_ENUM_CATEGORY_3D, PRINTER_ENUM_CATEGORY_ALL, PRINTER_ENUM_CONNECTIONS, PRINTER_ENUM_LOCAL, PRINTER_ENUM_NAME, PRINTER_ENUM_NETWORK, PRINTER_ENUM_REMOTE, PRINTER_ENUM_SHARED, _win32_EnumPrinters, gdi.enumprinters, winspool/EnumPrinters, winspool/EnumPrintersA, winspool/EnumPrintersW
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
req.unicode-ansi: EnumPrintersW (Unicode) and EnumPrintersA (ANSI)
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
api_name:
-	EnumPrinters
-	EnumPrintersA
-	EnumPrintersW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPrintersW function


## -description


The <b>EnumPrinters</b> function enumerates available printers, print servers, domains, or print providers.


## -parameters




### -param Flags [in]

The types of print objects that the function should enumerate. This value can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_LOCAL"></a><a id="printer_enum_local"></a><dl>
<dt><b>PRINTER_ENUM_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
If the PRINTER_ENUM_NAME flag is not also passed, the function ignores the <i>Name</i> parameter, and enumerates the locally installed printers. If PRINTER_ENUM_NAME is also passed, the function enumerates the local printers on <i>Name</i>. 

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_NAME"></a><a id="printer_enum_name"></a><dl>
<dt><b>PRINTER_ENUM_NAME</b></dt>
</dl>
</td>
<td width="60%">
The function enumerates the printer identified by <i>Name</i>. This can be a server, a domain, or a print provider. If <i>Name</i> is <b>NULL</b>, the function enumerates available print providers.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_SHARED"></a><a id="printer_enum_shared"></a><dl>
<dt><b>PRINTER_ENUM_SHARED</b></dt>
</dl>
</td>
<td width="60%">
The function enumerates printers that have the shared attribute. Cannot be used in isolation; use an OR operation to combine with another PRINTER_ENUM type.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_CONNECTIONS"></a><a id="printer_enum_connections"></a><dl>
<dt><b>PRINTER_ENUM_CONNECTIONS</b></dt>
</dl>
</td>
<td width="60%">

                   The function enumerates the list of printers to which the user has made previous connections.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_NETWORK"></a><a id="printer_enum_network"></a><dl>
<dt><b>PRINTER_ENUM_NETWORK</b></dt>
</dl>
</td>
<td width="60%">

                   The function enumerates network printers in the computer's domain. This value is valid only if <i>Level</i> is 1.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_REMOTE"></a><a id="printer_enum_remote"></a><dl>
<dt><b>PRINTER_ENUM_REMOTE</b></dt>
</dl>
</td>
<td width="60%">

                   The function enumerates network printers and print servers in the computer's domain. This value is valid only if <i>Level</i> is 1.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_CATEGORY_3D"></a><a id="printer_enum_category_3d"></a><dl>
<dt><b>PRINTER_ENUM_CATEGORY_3D</b></dt>
</dl>
</td>
<td width="60%">
The function enumerates only 3D printers.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_ENUM_CATEGORY_ALL"></a><a id="printer_enum_category_all"></a><dl>
<dt><b>PRINTER_ENUM_CATEGORY_ALL</b></dt>
</dl>
</td>
<td width="60%">
The function enumerates all print devices, including 3D printers.

</td>
</tr>
</table>
 

If <i>Level</i> is 4, you can only use the PRINTER_ENUM_CONNECTIONS and PRINTER_ENUM_LOCAL constants.

<div class="alert"><b>Note</b>  3D print devices are not enumerated by default. You must include both <b>PRINTER_ENUM_CATEGORY_3D</b> and <b>PRINTER_ENUM_LOCAL</b> to enumerate only 3D printers. To include 3D printers, along with all other local printers, use <b>PRINTER_ENUM_CATEGORY_ALL</b> and <b>PRINTER_ENUM_LOCAL</b>.</div>
<div> </div>

### -param Name [in]

If <i>Level</i> is 1, <i>Flags</i> contains PRINTER_ENUM_NAME, and <i>Name</i> is non-<b>NULL</b>, then <i>Name</i> is a pointer to a null-terminated string that specifies the name of the object to enumerate. This string can be the name of a server, a domain, or a print provider.

If <i>Level</i> is 1, <i>Flags</i> contains PRINTER_ENUM_NAME, and <i>Name</i> is <b>NULL</b>, then the function enumerates the available print providers.

If <i>Level</i> is 1, <i>Flags</i> contains PRINTER_ENUM_REMOTE, and <i>Name</i> is <b>NULL</b>, then the function enumerates the printers in the user's domain.

If <i>Level</i> is 2 or 5,<i>Name</i> is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated. If this string is <b>NULL</b>, then the function enumerates the printers installed on the local computer.

If <i>Level</i> is 4, <i>Name</i> should be <b>NULL</b>. The function always queries on the local computer.

When <i>Name</i> is <b>NULL</b>, setting <i>Flags</i> to PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS enumerates printers that are installed on the local machine. These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.

When <i>Name</i> is not <b>NULL</b>, setting <i>Flags</i> to PRINTER_ENUM_LOCAL | PRINTER_ENUM_NAME enumerates the local printers that are installed on the server <i>Name</i>.


### -param Level [in]

The type of data structures pointed to by <i>pPrinterEnum</i>. Valid values are 1, 2, 4, and 5, which correspond to the <a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>, <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> , <a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>, and <a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a> data structures.

This value can be 1, 2, 4, or 5.


### -param pPrinterEnum [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>, <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>, <a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>, or <a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a> structures. Each structure contains data that describes an available print object.

If <i>Level</i> is 1, the array contains <a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a> structures. If <i>Level</i> is 2, the array contains <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structures. If <i>Level</i> is 4, the array contains <a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a> structures. If <i>Level</i> is 5, the array contains <a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a> structures.

The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point. If the buffer is too small, the <i>pcbNeeded</i> parameter returns the required buffer size.


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pPrinterEnum</i>.


### -param pcbNeeded [out]

A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if <i>cbBuf</i> is too small.


### -param pcReturned [out]

A pointer to a value that receives the number of <a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>, <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> , <a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>, or <a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a> structures that the function returns in the array to which <i>pPrinterEnum</i> points.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



Do not call this method in <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>.

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
If <b>EnumPrinters</b> returns a <a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a> structure in which PRINTER_ENUM_CONTAINER is specified, this indicates that there is a hierarchy of printer objects. An application can enumerate the hierarchy by calling <b>EnumPrinters</b> again, setting <i>Name</i> to the value of the <b>PRINTER_INFO_1</b> structure's <b>pName</b> member.

The <b>EnumPrinters</b> function does not retrieve security information. If  <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structures are returned in the array pointed to by <i>pPrinterEnum</i>, their <i>pSecurityDescriptor</i> members will be set to <b>NULL</b>.


         To get information about the default printer, call <a href="https://msdn.microsoft.com/8ec06743-43ce-4fac-83c4-f09eac7ee333">GetDefaultPrinter</a>.


         The <a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a> structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established. When <b>EnumPrinters</b> is called with a <b>PRINTER_INFO_4</b> data structure, that function queries the registry for the specified information, then returns immediately. This differs from the behavior of <b>EnumPrinters</b> when called with other levels of <b>PRINTER_INFO_*</b> data structures. In particular, when <b>EnumPrinters</b> is called with a level 2 (<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>) data structure, it performs an <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> call on each remote connection. If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the <b>OpenPrinter</b> call. This can take a while. Passing a <b>PRINTER_INFO_4</b> structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent <b>EnumPrinters</b> level 2 call can be made.

<b>Windows Vista:</b> The printer data returned by <b>EnumPrinters</b> is retrieved from a local cache when the value of <i>Level</i> is 4.

The following table shows the <b>EnumPrinters</b> output for various <i>Flags</i> values when the <i>Level</i> parameter is set to 1.


In the <i>Name</i> parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine. For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider. To retrieve print provider names, call <b>EnumPrinters</b> with <i>Name</i> set to <b>NULL</b>. 



<table>
<tr>
<th><i>Flags</i> parameter</th>
<th><i>Name</i> parameter</th>
<th>Result</th>
</tr>
<tr>
<td>PRINTER_ENUM_LOCAL (and not PRINTER_ENUM_NAME)</td>
<td>
The <i>Name</i> parameter is ignored.

</td>
<td>
All local printers.

</td>
</tr>
<tr>
<td>PRINTER_ENUM_NAME</td>
<td>
"Print Provider"

</td>
<td>
All domain names

</td>
</tr>
<tr>
<td>PRINTER_ENUM_NAME</td>
<td>
 "Print Provider!Domain"

</td>
<td>
All printers and print servers in the computer's domain

</td>
</tr>
<tr>
<td>PRINTER_ENUM_NAME</td>
<td>
"Print Provider!!\\Machine"

</td>
<td>
All printers shared at \\Machine

</td>
</tr>
<tr>
<td>PRINTER_ENUM_NAME</td>
<td>
An empty string, ""

</td>
<td>
All local printers.

</td>
</tr>
<tr>
<td>PRINTER_ENUM_NAME</td>
<td>
<b>NULL</b>

</td>
<td>
All print providers in the computer's domain

</td>
</tr>
<tr>
<td>PRINTER_ENUM_CONNECTIONS</td>
<td>
The <i>Name</i> parameter is ignored.

</td>
<td>
All connected remote printers

</td>
</tr>
<tr>
<td>PRINTER_ENUM_NETWORK</td>
<td>
The <i>Name</i> parameter is ignored.

</td>
<td>
All printers in the computer's domain

</td>
</tr>
<tr>
<td>PRINTER_ENUM_REMOTE</td>
<td>
An empty string, ""

</td>
<td>
All printers and print servers in the computer's domain

</td>
</tr>
<tr>
<td>PRINTER_ENUM_REMOTE </td>
<td>
"Print Provider"

</td>
<td>
Same as PRINTER_ENUM_NAME

</td>
</tr>
<tr>
<td>PRINTER_ENUM_REMOTE</td>
<td>
"Print Provider!Domain"

</td>
<td>
All printers and print servers in computer's domain, regardless of <i>Domain</i> specified.

</td>
</tr>
<tr>
<td>PRINTER_ENUM_CATEGORY_3D</td>
<td>
The <i>Name</i> parameter is ignored.

</td>
<td>
Only 3D printers are enumerated.

</td>
</tr>
<tr>
<td>PRINTER_ENUM_CATEGORY_ALL</td>
<td>
The <i>Name</i> parameter is ignored.

</td>
<td>
3D printers are enumerated, along with all other printers.

</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>



<a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

