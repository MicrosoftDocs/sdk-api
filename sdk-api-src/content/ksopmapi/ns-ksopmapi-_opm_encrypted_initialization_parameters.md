---
UID: NS:ksopmapi._OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
title: "_OPM_ENCRYPTED_INITIALIZATION_PARAMETERS"
author: windows-sdk-content
description: Contains initialization parameters for an Output Protection Manager (OPM) session.
old-location: mf\opm_encrypted_initialization_parameters.htm
tech.root: medfound
ms.assetid: abcf0b84-7370-48da-b4dd-4faded6be343
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: OPM_ENCRYPTED_INITIALIZATION_PARAMETERS, OPM_ENCRYPTED_INITIALIZATION_PARAMETERS structure [Media Foundation], _OPM_ENCRYPTED_INITIALIZATION_PARAMETERS, ksopmapi/OPM_ENCRYPTED_INITIALIZATION_PARAMETERS, mf.opm_encrypted_initialization_parameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ksopmapi.h
req.include-header: Opmapi.h
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
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
product: Windows
targetos: Windows
req.typenames: OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
req.redist: 
---

# _OPM_ENCRYPTED_INITIALIZATION_PARAMETERS structure


## -description


Contains initialization parameters for an <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM) session.


## -struct-fields




### -field abEncryptedInitializationParameters

Pointer to a buffer that contains encrypted initialization parameters for the session. For more information, see <a href="https://msdn.microsoft.com/7551e374-8745-405b-9879-d35a92d661ea">IOPMVideoOutput::FinishInitialization</a>.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/eaf220cf-111f-42fa-80db-1c69cd863258">AMCOPPSignature</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

