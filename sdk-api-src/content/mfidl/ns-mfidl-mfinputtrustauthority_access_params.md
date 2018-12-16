---
UID: NS:mfidl._MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
title: MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
author: windows-sdk-content
description: Contains parameters for the IMFInputTrustAuthority::BindAccess or IMFInputTrustAuthority::UpdateAccess method.
old-location: mf\mfinputtrustauthority_access_params.htm
tech.root: medfound
ms.assetid: 5ff3ec3a-a7b1-4378-8e8b-d59a6f5bb28d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5ff3ec3a-a7b1-4378-8e8b-d59a6f5bb28d, MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS, MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS structure [Media Foundation], mf.mfinputtrustauthority_access_params, mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
product: Windows
targetos: Windows
req.typenames: MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
req.redist: 
---

# MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS structure


## -description



Contains parameters for the <a href="https://msdn.microsoft.com/94e447af-9311-4a2c-9ec5-be371684f79d">IMFInputTrustAuthority::BindAccess</a> or <a href="https://msdn.microsoft.com/4ca635fc-15eb-4a9e-8f59-7fa2e3f3e176">IMFInputTrustAuthority::UpdateAccess</a> method.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwVer

Version number. This value must be zero.


### -field cbSignatureOffset

Offset of the signature from the start of the structure, in bytes.


### -field cbSignatureSize

Size of the signature, in bytes.


### -field cbExtensionOffset

Offset of the extension blob from the start of the structure, in bytes.


### -field cbExtensionSize

Size of the extension blob, in bytes.


### -field cActions

Number of elements in the <b>rgOutputActions</b> array.


### -field rgOutputActions

Array of <a href="https://msdn.microsoft.com/24e74739-054c-46ef-8df7-b29a9a2ea94a">MFINPUTTRUSTAUTHORITY_ACCESS_ACTION</a> structures. The number of elements in the array is specified in the <b>cActions</b> member.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

