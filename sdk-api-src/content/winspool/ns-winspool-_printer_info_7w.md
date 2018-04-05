---
UID: NS:winspool._PRINTER_INFO_7W
title: "_PRINTER_INFO_7W"
author: windows-driver-content
description: The PRINTER_INFO_7 structure specifies directory services printer information.
old-location: gdi\printer_info_7.htm
old-project: printdocs
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_7W, *PPRINTER_INFO_7W, DSPRINT_PENDING, DSPRINT_PUBLISH, DSPRINT_REPUBLISH, DSPRINT_UNPUBLISH, DSPRINT_UPDATE, PPRINTER_INFO_7, PPRINTER_INFO_7 structure pointer [Windows GDI], PRINTER_INFO_7, PRINTER_INFO_7 structure [Windows GDI], PRINTER_INFO_7W, _PRINTER_INFO_7A, _PRINTER_INFO_7W, _win32_PRINTER_INFO_7_str, gdi.printer_info_7, winspool/PPRINTER_INFO_7, winspool/PRINTER_INFO_7, winspool/_PRINTER_INFO_7A, winspool/_PRINTER_INFO_7W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_PRINTER_INFO_7W (Unicode) and _PRINTER_INFO_7A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_7W, *PPRINTER_INFO_7W, *LPPRINTER_INFO_7W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_7
-	_PRINTER_INFO_7A
-	_PRINTER_INFO_7W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_7W structure


## -description




          The <b>PRINTER_INFO_7</b> structure specifies directory services printer information. Use this structure with the <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS. Use this structure with the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function to determine whether a printer is published in the DS.
        




## -struct-fields




### -field pszObjectGUID


            A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer. Use the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function to retrieve this GUID.


              Before calling <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>, set <b>pszObjectGUID</b> to <b>NULL</b>.
            


### -field dwAction


            Indicates the action for the <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> function to
            perform. For the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function, this member indicates
            whether the specified printer is published. This member can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DSPRINT_PENDING"></a><a id="dsprint_pending"></a><dl>
<dt><b>DSPRINT_PENDING</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>: Indicates that the system is attempting to complete a publish or unpublish operation started by a <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> call.


<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>: This value is not valid.
                  

</td>
</tr>
<tr>
<td width="40%"><a id="DSPRINT_PUBLISH"></a><a id="dsprint_publish"></a><dl>
<dt><b>DSPRINT_PUBLISH</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>: Publishes the printer's data in the DS.


<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>: Indicates the printer is published.
                  

</td>
</tr>
<tr>
<td width="40%"><a id="DSPRINT_REPUBLISH"></a><a id="dsprint_republish"></a><dl>
<dt><b>DSPRINT_REPUBLISH</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>: The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer. Re-publishing also changes the GUID of the published printer.


<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>: Never returns this value.
                  

</td>
</tr>
<tr>
<td width="40%"><a id="DSPRINT_UNPUBLISH"></a><a id="dsprint_unpublish"></a><dl>
<dt><b>DSPRINT_UNPUBLISH</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>: Removes the printer's published data from the DS.


<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>: Indicates the printer is not published.
                  

</td>
</tr>
<tr>
<td width="40%"><a id="DSPRINT_UPDATE"></a><a id="dsprint_update"></a><dl>
<dt><b>DSPRINT_UPDATE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>: Updates the printer's published data in the DS.


<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>: Never returns this value.
                  

</td>
</tr>
</table>
 


## -remarks




        The <b>PRINTER_INFO_7</b> structure is used in a <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> call to publish printer information to the directory service. The published data includes all values and data for the specified printer found under the SPLDS_SPOOLER_KEY, SPLDS_DRIVER_KEY, or SPLDS_USER_KEY keys created by <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a>.
      


        For <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>, <i>pszObjectGUID</i> should be set to <b>NULL</b>. For <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>, <i>pszObjectGUID</i> returns the GUID of the directory services print queue object associated with a published printer. You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer. However, the recommended method for retrieving published data is to call the <a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a> function.
      




## -see-also




<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

