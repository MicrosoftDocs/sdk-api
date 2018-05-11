---
UID: NS:strmif._AMCOPPCommand
title: "_AMCOPPCommand"
author: windows-driver-content
description: The AMCOPPCommand structure contains a Certified Output Protection Protocol (COPP) command.
old-location: dshow\amcoppcommand.htm
old-project: DirectShow
ms.assetid: 8b2c06e9-f1b7-4185-8ade-b5abe9ac776d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*LPAMCOPPCommand, AMCOPPCommand, AMCOPPCommand structure [DirectShow], AMCOPPCommandStructure, LPAMCOPPCommand, LPAMCOPPCommand structure pointer [DirectShow], _AMCOPPCommand, dshow.amcoppcommand, strmif/AMCOPPCommand, strmif/LPAMCOPPCommand"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.typenames: AMCOPPCommand, *LPAMCOPPCommand
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	AMCOPPCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP
---

# _AMCOPPCommand structure


## -description



The AMCOPPCommand structure contains a Certified Output Protection Protocol (COPP) command.




## -struct-fields




### -field macKDI

Message Authentication Code (MAC) of the command data. Use AES-based one-key CBC MAC (OMAC) to calculate this value.


### -field guidCommandID

GUID that specifies the command.


### -field dwSequence

Sequence number. The application must keep a running count of the COPP commands issued. For each command, increment the sequence number by one.


### -field cbSizeData

Number of bytes of valid data in the <b>CommandData</b> member.


### -field CommandData

Data for the command. The meaning of the data depends on the command.


## -remarks



The following COPP commands are defined.

<table>
<tr>
<th><b>GUID</b></th>
<th>Description
            </th>
</tr>
<tr>
<td>DXVA_COPPSetProtectionLevel</td>
<td>Sets a specified protection type to a specified protection level.</td>
</tr>
</table>
 

For more information, see the Windows DDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

