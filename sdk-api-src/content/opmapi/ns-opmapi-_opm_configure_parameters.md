---
UID: NS:opmapi._OPM_CONFIGURE_PARAMETERS
title: "_OPM_CONFIGURE_PARAMETERS"
author: windows-driver-content
description: Contains an Output Protection Manager (OPM) or Certified Output Protection Manager (COPP) command.
old-location: mf\opm_configure_parameters.htm
old-project: medfound
ms.assetid: 60d13945-740f-46bd-9602-bacd0dac5e32
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: OPM_CONFIGURE_PARAMETERS, OPM_CONFIGURE_PARAMETERS structure [Media Foundation], _OPM_CONFIGURE_PARAMETERS, mf.opm_configure_parameters, opmapi/OPM_CONFIGURE_PARAMETERS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: opmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OPM_CONFIGURE_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	opmapi.h
api_name:
-	OPM_CONFIGURE_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _OPM_CONFIGURE_PARAMETERS structure


## -description


Contains an <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM) or Certified Output Protection Manager (COPP) command.


## -struct-fields




### -field omac

An <a href="https://msdn.microsoft.com/6ff37a2a-9e63-4097-8ee6-bcc4bd580ab8">OPM_MAC</a> structure. Fill in this structure with the Message Authentication Code (MAC) of the command data. Use AES-based one-key CBC MAC (OMAC) to calculate this value.


### -field guidSetting

A GUID that specifies the command. For more information, see <a href="https://msdn.microsoft.com/52165e1b-a178-4483-bf76-4197281f856d">OPM Commands</a>.


### -field ulSequenceNumber

A command sequence number. The application must keep a running count of the commands issued. For each command, increment the sequence number by one.

On the first call to <a href="https://msdn.microsoft.com/b8eb3561-7e81-4f4c-bcb1-1657f8556aea">IOPMVideoOutput::Configure</a>, set <b>ulSequenceNumber</b> equal to the starting command 	sequence number, which is specified when the application calls <a href="https://msdn.microsoft.com/eeedeb4b-753f-4efb-b8ef-732cce116b42">IOPMVideoOutput::FinishInitialization</a>. On each subsequent call, increment <b>ulSequenceNumber</b> by 1.

Exception: If the <a href="https://msdn.microsoft.com/b8eb3561-7e81-4f4c-bcb1-1657f8556aea">IOPMVideoOutput::Configure</a> method fails, do not increment the sequence number. Instead, re-use the same number for the next command.


### -field cbParametersSize

The number of bytes of valid data in the <b>abParameters</b> member.


### -field abParameters

The data for the command. The meaning of the data depends on the command. For more information, see <a href="https://msdn.microsoft.com/52165e1b-a178-4483-bf76-4197281f856d">OPM Commands</a>.


## -remarks




        The layout of this  structure is identical to the <a href="https://msdn.microsoft.com/8b2c06e9-f1b7-4185-8ade-b5abe9ac776d">AMCOPPCommand</a> structure used in Certified Output Protection Protocol (COPP).
      

Initialize this structure as follows.

<ol>
<li>Fill in all the structure members except the <b>omac</b> member.</li>
<li>Use the OMAC 1 algorithm to calculate a message authentication code (MAC) for the block of data that appears after the <b>omac</b> member (excluding the <b>omac</b> member).</li>
<li>Copy the MAC to the <b>omac</b> member.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/b8eb3561-7e81-4f4c-bcb1-1657f8556aea">IOPMVideoOutput::Configure</a>



<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

