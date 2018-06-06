---
UID: NS:iketypes.IKEEXT_CIPHER_ALGORITHM0_
title: IKEEXT_CIPHER_ALGORITHM0_
author: windows-sdk-content
description: Stores information about the IKE/AuthIP encryption algorithm.
old-location: fwp\ikeext_cipher_algorithm0.htm
old-project: FWP
ms.assetid: 940714a3-d098-4d02-9209-fcf3b24ee4e7
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IKEEXT_CIPHER_ALGORITHM0, IKEEXT_CIPHER_ALGORITHM0 structure [Filtering], IKEEXT_CIPHER_ALGORITHM0_, fwp.ikeext_cipher_algorithm0, iketypes/IKEEXT_CIPHER_ALGORITHM0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IKEEXT_CIPHER_ALGORITHM0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CIPHER_ALGORITHM0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_CIPHER_ALGORITHM0_ structure


## -description


The <b>IKEEXT_CIPHER_ALGORITHM0</b> structure stores information about the IKE/AuthIP encryption algorithm.


## -struct-fields




### -field algoIdentifier

The type of encryption algorithm.

See <a href="https://msdn.microsoft.com/00d5def0-5c8c-4d84-b929-aec76a1a7110">IKEEXT_CIPHER_TYPE</a> for more information.


### -field keyLen

Unused parameter, always set it to 0.


### -field rounds

Unused parameter, always set it to 0.


## -remarks



<b>IKEEXT_CIPHER_ALGORITHM0</b> is a specific implementation of IKEEXT_CIPHER_ALGORITHM. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/00d5def0-5c8c-4d84-b929-aec76a1a7110">IKEEXT_CIPHER_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

