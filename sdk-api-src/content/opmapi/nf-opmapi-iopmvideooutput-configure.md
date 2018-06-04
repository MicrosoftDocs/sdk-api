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
 

 

