---
UID: NF:opmapi.IOPMVideoOutput.Configure
title: IOPMVideoOutput::Configure
author: windows-sdk-content
description: Configures a video output.
old-location: mf\iopmvideooutput_iopmvideooutput__configure.htm
tech.root: medfound
ms.assetid: b8eb3561-7e81-4f4c-bcb1-1657f8556aea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Configure, Configure method [Media Foundation], Configure method [Media Foundation],IOPMVideoOutput interface, IOPMVideoOutput interface [Media Foundation],Configure method, IOPMVideoOutput.Configure, IOPMVideoOutput::Configure, mf.iopmvideooutput_iopmvideooutput__configure, opmapi/IOPMVideoOutput::Configure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - opmapi.h
api_name:
 - IOPMVideoOutput.Configure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOPMVideoOutput::Configure


## -description


Configures a video output. This method sends an Output Protection Manager (OPM) or Certified Output Protection Protocol (COPP) command to the driver.


## -parameters




### -param pParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/60d13945-740f-46bd-9602-bacd0dac5e32">OPM_CONFIGURE_PARAMETERS</a> structure that contains the command. For a list of OPM commands, see <a href="https://msdn.microsoft.com/52165e1b-a178-4483-bf76-4197281f856d">OPM Commands</a>.


### -param ulAdditionalParametersSize [in]

The size of the <i>pbAdditionalParameters</i> buffer, in bytes.


### -param pbAdditionalParameters [in]

Pointer to a buffer that contains additional information for the command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is equivalent to the <b>IAMCertifiedOutputProtection::ProtectionCommand</b> method in COPP.

This method supports both OPM semantics and COPP semantics. COPP semantics are supported for backward compatibility; new applications should use OPM semantics.

<h3><a id="OPM_Semantics"></a><a id="opm_semantics"></a><a id="OPM_SEMANTICS"></a>OPM Semantics</h3>
Some OPM commands require additional configuration information to be passed in the <i>pbAdditionalParameters</i> parameter. The <i>ulAdditionalParametersSize</i> parameter specifies the size of the additional data.

<h3><a id="COPP_Semantics"></a><a id="copp_semantics"></a><a id="COPP_SEMANTICS"></a>COPP Semantics</h3>
The <i>pbAdditionalParameters</i> parameter must be <b>NULL</b>, and <i>ulAdditionalParametersSize</i> must be zero.




## -see-also




<a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

