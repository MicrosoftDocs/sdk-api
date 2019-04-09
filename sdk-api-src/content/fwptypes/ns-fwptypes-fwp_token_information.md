---
UID: NS:fwptypes.FWP_TOKEN_INFORMATION_
title: FWP_TOKEN_INFORMATION (fwptypes.h)
author: windows-sdk-content
description: The FWP_TOKEN_INFORMATION structure defines a set of security identifiers that are used for user-mode classification.
old-location: fwp\fwp_token_information.htm
tech.root: fwp
ms.assetid: 30bc6d4b-e3a8-4adf-82d5-adaf30f042ff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWP_TOKEN_INFORMATION, FWP_TOKEN_INFORMATION structure [Filtering], fwp.fwp_token_information, fwptypes/FWP_TOKEN_INFORMATION
ms.topic: struct
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
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
 - Fwptypes.h
api_name:
 - FWP_TOKEN_INFORMATION
product: Windows
targetos: Windows
req.typenames: FWP_TOKEN_INFORMATION
req.redist: 
---

# FWP_TOKEN_INFORMATION structure


## -description


The <b>FWP_TOKEN_INFORMATION</b> structure defines a set of security identifiers that are used for user-mode classification.


## -struct-fields




### -field sidCount

The number of <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures stored in the <b>sids</b> array.


### -field sids

An array of <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures containing user and group security information.


### -field restrictedSidCount

The number of <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures stored in the <b>restrictedSids</b> array.


### -field restrictedSids

An array of <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures containing restricted SIDs security information.

