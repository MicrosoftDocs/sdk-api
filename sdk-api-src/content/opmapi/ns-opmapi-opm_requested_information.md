---
UID: NS:opmapi._OPM_REQUESTED_INFORMATION
title: OPM_REQUESTED_INFORMATION (opmapi.h)
author: windows-sdk-content
description: Contains the result of an Output Protection Manager (OPM) status request.
old-location: mf\opm_requested_information.htm
tech.root: medfound
ms.assetid: 84ffa808-1bdb-47c8-a18c-6dfa6fcf90de
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OPM_REQUESTED_INFORMATION, OPM_REQUESTED_INFORMATION structure [Media Foundation], _OPM_REQUESTED_INFORMATION, ksopmapi/OPM_REQUESTED_INFORMATION, mf.opm_requested_information
ms.topic: struct
req.header: opmapi.h
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
 - OPM_REQUESTED_INFORMATION
product: Windows
targetos: Windows
req.typenames: OPM_REQUESTED_INFORMATION
req.redist: 
---

# OPM_REQUESTED_INFORMATION structure


## -description


Contains the result of an <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM) status request.


## -struct-fields




### -field omac

An <a href="https://msdn.microsoft.com/6ff37a2a-9e63-4097-8ee6-bcc4bd580ab8">OPM_OMAC</a> structure that contains a Message Authentication Code (MAC) of the status data. The driver will use AES-based one-key CBC MAC (OMAC) to calculate this value.


### -field cbRequestedInformationSize

The size of the valid data in the <b>abRequestedInformation</b> member, in bytes.


### -field abRequestedInformation

A buffer that contains the result of the status request. The meaning of the data depends on the status request. For more information, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/en-us/library/Dd373428(v=VS.85).aspx">AMCOPPStatusOutput</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">IOPMVideoOutput::COPPCompatibleGetInformation</a>



<a href="https://msdn.microsoft.com/47d724eb-07e9-4659-886a-4b492fbb2415">IOPMVideoOutput::GetInformation</a>



<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

