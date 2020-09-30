---
UID: NS:opmapi._OPM_CONFIGURE_PARAMETERS
title: OPM_CONFIGURE_PARAMETERS (opmapi.h)
description: Contains an Output Protection Manager (OPM) or Certified Output Protection Manager (COPP) command.
helpviewer_keywords: ["OPM_CONFIGURE_PARAMETERS","OPM_CONFIGURE_PARAMETERS structure [Media Foundation]","mf.opm_configure_parameters","opmapi/OPM_CONFIGURE_PARAMETERS"]
old-location: mf\opm_configure_parameters.htm
tech.root: mf
ms.assetid: 60d13945-740f-46bd-9602-bacd0dac5e32
ms.date: 12/05/2018
ms.keywords: OPM_CONFIGURE_PARAMETERS, OPM_CONFIGURE_PARAMETERS structure [Media Foundation], mf.opm_configure_parameters, opmapi/OPM_CONFIGURE_PARAMETERS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPM_CONFIGURE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_CONFIGURE_PARAMETERS
 - opmapi/_OPM_CONFIGURE_PARAMETERS
 - OPM_CONFIGURE_PARAMETERS
 - opmapi/OPM_CONFIGURE_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_CONFIGURE_PARAMETERS
---

# OPM_CONFIGURE_PARAMETERS structure


## -description

Contains an <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM) or Certified Output Protection Manager (COPP) command.

## -struct-fields

### -field omac

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac">OPM_MAC</a> structure. Fill in this structure with the Message Authentication Code (MAC) of the command data. Use AES-based one-key CBC MAC (OMAC) to calculate this value.

### -field guidSetting

A GUID that specifies the command. For more information, see <a href="/windows/desktop/medfound/opm-commands">OPM Commands</a>.

### -field ulSequenceNumber

A command sequence number. The application must keep a running count of the commands issued. For each command, increment the sequence number by one.

On the first call to <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure">IOPMVideoOutput::Configure</a>, set <b>ulSequenceNumber</b> equal to the starting command 	sequence number, which is specified when the application calls <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization">IOPMVideoOutput::FinishInitialization</a>. On each subsequent call, increment <b>ulSequenceNumber</b> by 1.

Exception: If the <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure">IOPMVideoOutput::Configure</a> method fails, do not increment the sequence number. Instead, re-use the same number for the next command.

### -field cbParametersSize

The number of bytes of valid data in the <b>abParameters</b> member.

### -field abParameters

The data for the command. The meaning of the data depends on the command. For more information, see <a href="/windows/desktop/medfound/opm-commands">OPM Commands</a>.

## -remarks

The layout of this  structure is identical to the <a href="/windows/desktop/api/strmif/ns-strmif-amcoppcommand">AMCOPPCommand</a> structure used in Certified Output Protection Protocol (COPP).
      

Initialize this structure as follows.

<ol>
<li>Fill in all the structure members except the <b>omac</b> member.</li>
<li>Use the OMAC 1 algorithm to calculate a message authentication code (MAC) for the block of data that appears after the <b>omac</b> member (excluding the <b>omac</b> member).</li>
<li>Copy the MAC to the <b>omac</b> member.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure">IOPMVideoOutput::Configure</a>



<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>